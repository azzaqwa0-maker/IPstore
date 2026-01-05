<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Simulasi Jualan iPhone</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #111;
        color: white;
        padding: 20px;
    }
    h1 {
        text-align: center;
    }
    .box {
        background: #1e1e1e;
        padding: 15px;
        border-radius: 10px;
        margin-bottom: 15px;
    }
    select, input, button {
        width: 100%;
        padding: 10px;
        margin-top: 10px;
        border-radius: 8px;
        border: none;
        font-size: 16px;
    }
    button {
        background: #00c853;
        color: black;
        font-weight: bold;
        cursor: pointer;
    }
    .hasil {
        margin-top: 15px;
        font-size: 18px;
    }
</style>
</head>
<body>

<h1>📱 Simulasi Jualan iPhone</h1>

<div class="box">
    <label>Pilih iPhone:</label>
    <select id="hp">
        <option value="17000000">iPhone 17 Pro Max - Rp14.000.000</option>
        <option value="8500000">iPhone 13 Mini - Rp7.500.000</option>
        <option value="12000000">iPhone 13 Pro - Rp10.000.000</option>
        <option value="6000000">iPhone 11 - Rp4.000.000</option>
    </select>

    <label>Jumlah:</label>
    <input type="number" id="jumlah" value="1" min="1">

    <button onclick="pesan()">Pesan Sekarang</button>

    <div class="hasil" id="hasil"></div>
</div>

<script>
function formatRupiah(angka) {
    return angka.toLocaleString("id-ID");
}

function pesan() {
    let harga = parseInt(document.getElementById("hp").value);
    let jumlah = parseInt(document.getElementById("jumlah").value);
    let total = harga * jumlah;

    document.getElementById("hasil").innerHTML = `
        Total Harga: <b>Rp ${formatRupiah(total)}</b>
    `;
}
</script>

</body>
</html>

