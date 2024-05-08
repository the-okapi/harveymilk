<script>
    export let question;
    let picked = [false, false, false, false];
    let answered = false;
    /**
	 * @param {number} pick
	 */
    function answer(pick) {
        picked[pick] = true;
        answered = true;
        console.log("picked");
    } 
</script>

<div class="triviaBox">
    <p>{question.text}</p>
    <div class="buttonContainer">
        {#if answered}
            {#if question.answer == 0}
                <button class="bGreen">{question.options[0]}</button>
            {:else if picked[0] == true}
                <button class="bRed">{question.options[0]}</button>
            {:else}
                <button>{question.options[0]}</button>
            {/if}
        {:else}
            <button on:click={() => {answer(0)}}>{question.options[0]}</button>
        {/if}
        {#if answered}
            {#if question.answer == 1}
                <button class="bGreen">{question.options[1]}</button>
            {:else if picked[1] == true}
                <button class="bRed">{question.options[1]}</button>
            {:else}
                <button>{question.options[1]}</button>
            {/if}
        {:else}
            <button on:click={() => {answer(1)}}>{question.options[1]}</button>
        {/if}
        {#if answered}
            {#if question.answer == 2}
                <button class="bGreen">{question.options[2]}</button>
            {:else if picked[2] == true}
                <button class="bRed">{question.options[2]}</button>
            {:else}
                <button>{question.options[2]}</button>
            {/if}
        {:else}
            <button on:click={() => {answer(2)}}>{question.options[2]}</button>
        {/if}
        {#if answered}
            {#if question.answer == 3}
                <button class="bGreen">{question.options[3]}</button>
            {:else if picked[3] == true}
                <button class="bRed">{question.options[3]}</button>
            {:else}
                <button>{question.options[3]}</button>
            {/if}
        {:else}
            <button on:click={() => {answer(3)}}>{question.options[3]}</button>
        {/if}
    </div>
</div>