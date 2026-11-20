<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Preventivo - MHM System</title>
<style>
  * { box-sizing: border-box; }
  body { font-family: -apple-system, Helvetica, Arial, sans-serif; margin: 0; padding: 16px; background: #f2f2f2; color: #222; }
  .foglio { max-width: 820px; margin: 0 auto; background: #fff; padding: 20px; border-radius: 8px; }
  .intestazione { border-bottom: 3px solid #1a5fb4; padding-bottom: 12px; margin-bottom: 16px; }
  .intestazione h1 { margin: 0 0 6px 0; color: #1a5fb4; font-size: 22px; }
  .intestazione p { margin: 2px 0; font-size: 13px; }
  .riga2 { display: flex; gap: 12px; flex-wrap: wrap; }
  .riga2 > div { flex: 1; min-width: 200px; }
  label { display: block; font-size: 12px; color: #555; margin-top: 8px; }
  input, textarea { width: 100%; padding: 8px; font-size: 15px; border: 1px solid #bbb; border-radius: 6px; }
  table { width: 100%; border-collapse: collapse; margin-top: 14px; }
  th { background: #1a5fb4; color: #fff; font-size: 12px; padding: 6px; text-align: left; }
  td { padding: 4px; border-bottom: 1px solid #ddd; vertical-align: top; }
  td input, td textarea { padding: 6px; font-size: 14px; }
  td.num { width: 80px; }
  td.tot { width: 90px; text-align: right; font-weight: bold; padding-top: 12px; }
  button { padding: 10px 14px; font-size: 15px; border: none; border-radius: 6px; background: #1a5fb4; color: #fff; margin: 10px 6px 0 0; }
  button.sec { background: #777; }
  button.del { background: #c01c28; padding: 6px 10px; margin: 0; }
  .totali { margin-top: 16px; text-align: right; }
  .totali p { margin: 4px 0; font-size: 15px; }
  .totali .grande { font-size: 19px; font-weight: bold; color: #1a5fb4; }
  .iva { width: 70px; display: inline-block; text-align: right; }
  @media print {
    body { background: #fff; padding: 0; }
    .foglio { box-shadow: none; padding: 0; }
    button, .noprint { display: none !important; }
    input, textarea { border: none; padding: 2px; resize: none; }
  }
</style>
</head>
<body>
<div class="foglio">

  <div class="intestazione">
    <h1>MHM System di Hicham Charqane</h1>
    <p>Via San Benedetto 43 - 12070 Priola (CN)</p>
    <p>P.IVA 03826590048 - CF CHRHHM83R03Z330Z</p>
    <p>Cell 3333763643 - Mail mhm.system2019@gmail.com</p>
    <p>PEC charqane.hicham@pec.it - Codice univoco KRRH6B9</p>
  </div>

  <h2>PREVENTIVO</h2>
  <div class="riga2">
    <div><label>Numero preventivo</label><input id="numero" placeholder="es. 2026/001"></div>
    <div><label>Data</label><input id="data" type="date"></div>
  </div>

  <h3>Cliente</h3>
  <div class="riga2">
    <div><label>Nome / Ragione sociale</label><input id="cliente"></div>
    <div><label>Telefono</label><input id="tel" type="tel"></div>
  </div>
  <label>Indirizzo</label><input id="indirizzo">
  <label>Oggetto dei lavori</label><input id="oggetto" placeholder="es. Impianto fotovoltaico 6 kW">

  <table>
    <thead>
      <tr><th>Descrizione</th><th>Q.tà</th><th>Prezzo €</th><th>Totale €</th><th class="noprint"></th></tr>
    </thead>
    <tbody id="voci"></tbody>
  </table>
  <button onclick="aggiungiRiga()" class="noprint">+ Aggiungi voce</button>

  <div class="totali">
    <p>Imponibile: <strong id="imponibile">0,00</strong> €</p>
    <p>IVA <input id="aliquota" class="iva" type="number" value="22" oninput="calcola()"> %: <strong id="iva">0,00</strong> €</p>
    <p class="grande">Totale: <span id="totale">0,00</span> €</p>
  </div>

  <label>Condizioni, tempi e validità dell'offerta</label>
  <textarea id="condizioni" rows="4">Validità dell'offerta: 30 giorni. Pagamento: 30% all'ordine, saldo a fine lavori. Lavori eseguiti a regola d'arte secondo le norme CEI vigenti, con rilascio della dichiarazione di conformità.</textarea>

  <div class="noprint">
    <button onclick="window.print()">Stampa / Salva PDF</button>
    <button class="sec" onclick="salva()">Salva bozza</button>
    <button class="sec" onclick="nuovo()">Nuovo preventivo</button>
  </div>

</div>

<script>
function fmt(n) { return n.toLocaleString('it-IT', {minimumFractionDigits: 2, maximumFractionDigits: 2}); }

function aggiungiRiga(desc, qta, prezzo) {
  var tr = document.createElement('tr');
  tr.innerHTML =
    '<td><textarea rows="2" placeholder="Descrizione"></textarea></td>' +
    '<td class="num"><input type="number" step="any" value="1" oninput="calcola()"></td>' +
    '<td class="num"><input type="number" step="any" value="0" oninput="calcola()"></td>' +
    '<td class="tot">0,00</td>' +
    '<td class="noprint"><button class="del" onclick="this.closest(\'tr\').remove(); calcola();">X</button></td>';
  document.getElementById('voci').appendChild(tr);
  if (desc !== undefined) {
    tr.querySelector('textarea').value = desc;
    var inp = tr.querySelectorAll('input');
    inp[0].value = qta; inp[1].value = prezzo;
  }
  calcola();
}

function calcola() {
  var imponibile = 0;
  document.querySelectorAll('#voci tr').forEach(function(tr) {
    var inp = tr.querySelectorAll('input');
    var t = (parseFloat(inp[0].value) || 0) * (parseFloat(inp[1].value) || 0);
    tr.querySelector('.tot').textContent = fmt(t);
    imponibile += t;
  });
  var aliq = parseFloat(document.getElementById('aliquota').value) || 0;
  var iva = imponibile * aliq / 100;
  document.getElementById('imponibile').textContent = fmt(imponibile);
  document.getElementById('iva').textContent = fmt(iva);
  document.getElementById('totale').textContent = fmt(imponibile + iva);
}

function salva() {
  var voci = [];
  document.querySelectorAll('#voci tr').forEach(function(tr) {
    var inp = tr.querySelectorAll('input');
    voci.push([tr.querySelector('textarea').value, inp[0].value, inp[1].value]);
  });
  var d = {
    numero: numero.value, data: data.value, cliente: cliente.value, tel: tel.value,
    indirizzo: indirizzo.value, oggetto: oggetto.value, aliquota: aliquota.value,
    condizioni: condizioni.value, voci: voci
  };
  localStorage.setItem('bozzaPreventivo', JSON.stringify(d));
  alert('Bozza salvata su questo dispositivo.');
}

function carica() {
  var s = localStorage.getItem('bozzaPreventivo');
  if (!s) { aggiungiRiga(); return; }
  var d = JSON.parse(s);
  numero.value = d.numero; data.value = d.data; cliente.value = d.cliente; tel.value = d.tel;
  indirizzo.value = d.indirizzo; oggetto.value = d.oggetto; aliquota.value = d.aliquota;
  condizioni.value = d.condizioni;
  d.voci.forEach(function(v) { aggiungiRiga(v[0], v[1], v[2]); });
  if (!d.voci.length) aggiungiRiga();
  calcola();
}

function nuovo() {
  if (confirm('Cancellare tutto e iniziare un nuovo preventivo?')) {
    localStorage.removeItem('bozzaPreventivo');
    location.reload();
  }
}

data.value = new Date().toISOString().slice(0, 10);
carica();
</script>
</body>
</html>