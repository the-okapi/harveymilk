<script>
    import TopBar from '$lib/TopBar.svelte';
    import BottomBar from '$lib/BottomBar.svelte';
    import TriviaQuestion from '$lib/TriviaQuestion.svelte';
    import questions from '$lib/trivia.json';
</script>

<TopBar />
<div class="triviaContainer">

    {#each questions.questions as question}
        <TriviaQuestion question={question} />
    {/each}

    <p>Reload page to restart trivia</p>
</div>

<BottomBar />