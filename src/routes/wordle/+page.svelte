<script>
    import TopBar from '$lib/TopBar.svelte';
    import BottomBar from '$lib/BottomBar.svelte';
    import words from '$lib/words.json';
    function randNum() {
        let num = 1000;
        while (num >= words.length) {
            num = Math.floor(Math.random() * words.length)
        }
        return num;
    }
    let toGuess = words[randNum()];
    let letters = getLetters(toGuess);
    function redoWord() {
        toGuess = words[randNum()];
        letters = getLetters(toGuess);
    }
    function getLetters(ofWhat) {
        let toReturn = [];
        for (let i = 0; i < ofWhat.length; i++) {
            toReturn.push(ofWhat[i]);
        }
        return toReturn;
    }
    let done = false;
    let text = '';
    let hidden = false;
    let word = '';
    let oword = '';
    let classes = [];
    let content = [];
    let row = 0;
    for (let i = 0; i < 6; i++) {
        let claToAdd = [];
        let conToAdd = [];
        for (let j = 0; j < 6; j++) {
            claToAdd.push('wordleEmpty');
            conToAdd.push('');
        }
        classes.push(claToAdd);
        content.push(conToAdd);
    }
    function guess() {
        type();
        if (word.length > 6) {
            text = 'Word guessed is too long';
        } else if (word.length < 6) {
            text = 'Word is too short';
        } else {
            for (let i = 0; i < 6; i++) {
                if (word[i] === undefined) {
                    content[row][i] = ' ';    
                } else {
                    if (word[i] === toGuess[i]) {
                        classes[row][i] = 'wordleGreen';
                        const f = (element) => element === word[i];
                        letters.splice(letters.findIndex(f), 1);
                    } else if (letters.includes(word[i])) {
                        const f = (element) => element === word[i];
                        letters.splice(letters.findIndex(f), 1);
                        classes[row][i] = 'wordleYellow';
                    } else {
                        classes[row][i] = 'wordleWrong';
                    }
                    content[row][i] = word[i];
                }
            }
            letters = getLetters(toGuess);
            let notAll = true;
            for (let i = 0; i < word.length; i++) {
                if (classes[row][i] !== 'wordleGreen') {
                    notAll = false;
                    break;
                }
            }
            row++;
            if (row === 6) {
                done = true;
                hidden = true;
                text = 'You exceeded the maximum number of guesses. The word was \''+toGuess+'\'';
            }
            if (notAll) {
                done = true;
                hidden = true;
                text = 'Congratulations! You won the wordle!';
            }
            word = '';
            oword = '';
        }
    }
    function type() {
        word = oword.toUpperCase();
        for (let i = 0; i < 6; i++) {
            if (word[i] === undefined) {
                content[row][i] = '';
            } else {
                content[row][i] = word[i];
            }
        }
    }
    function reveal() {
        text = 'The word was \''+toGuess+'\'';
        hidden = true;
        done = true;
    }
    function restart() {
        location.reload();
    }
</script>

<TopBar />

<div class="wordleContainer">
    <div class="wordleBox">
        <div hidden={hidden}>
            <input type="text" on:keyup={type} bind:value={oword} on:click="{event => event.target.select()}" placeholder="Guess a Word"><button on:click={guess}>Guess</button>
        </div>
        {#if done}
            <button on:click={restart}>New Game</button>
        {/if}
        <p>{text}</p>
        {#each classes as cRow, i}
            <div class="wordleRow">
                {#each cRow as cCol, j}
                    <div class={cCol}><span class="wordleText">{content[i][j]}</span></div>
                {/each}
            </div>
        {/each}
        {#if !done}
            <button on:click={reveal}>Reveal Word</button>
        {/if}
    </div>
</div>

<BottomBar />