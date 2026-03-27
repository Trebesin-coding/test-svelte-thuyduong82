<script>
// Až vytvoříš komponent, nezapomeň jej importovat
// Emoji se vytváří pomocí windows + . nebo je můžeš zkopírovat odsud 🙂 😢
let score =$state(0)
let isHappy = $state(false)
let password = $state("🙂")
let emoji = $state("🙂")

function pricteni(){
    score+= 1
}
function zmena_emoji(){
    if(pasword==="heslo"){
        isHappy = true
    }
}

</script>

<div class="headings"></div>
<h3>git ad</h3>


<div class="container">
    <p>Zde se bude zobrazovat počet kliknutí:{score}</p> 
    <div class="buttons">
        <button onclick={pricteni}>zmackni na pricteni</button>
        <button onclick={zmena_emoji}>zmackni na zmenu emoji {emoji}</button>

        <input bind:value ={password}>
    </div>
</div>
{isHappy}?="🙂":"😢"


<style>
p{
    border: 1px solid black;
    color: black;
}

* {
    font-family: monospace;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    gap: 10px;
}

.container > p {
    font-size: 2em;
}

.buttons > button{
    border: 1px solid black;
    border-radius: 50000px;
    padding: 10px 20px;
    background-color: lightblue;
    font-size: 1.5em;
}

.buttons > button:nth-of-type(1) {
    background-color: lightblue;
}

.buttons > button:nth-of-type(2) {
    background-color: lightcoral;
}

.headings {
    position: absolute;
}

:global(.headings > h2) {
	position: absolute;
    font-size: 3em;

}

:global(.headings > h2:nth-child(1)) {
	left: 300px;
	top: 50px;
}

:global(.headings > h2:nth-child(2)) {
	left: 200px;
	top: 200px;
}

:global(.headings > h2:nth-child(3)) {
	left: 300px;
	top: 350px;
}


</style>