{cards}

<script>
function sleep(ms) {
  return new Promise(r => setTimeout(r, ms));
}


(async function () {

await sleep(1000)
x = document.getElementsByClassName('cards')[0].innerHTML
cards = JSON.parse(x)

async function f() {
    i = Math.floor(Math.random() * cards.length);
    [q,a] = cards[i];
    document.getElementsByClassName('cards')[0].innerHTML = q;
    await sleep(2000);
    document.getElementsByClassName('cards')[0].innerHTML = q + '<br>' + a;
    
    setTimeout(f, 2000);
}
    
setTimeout(f, 2000);
    
})()
</script>
