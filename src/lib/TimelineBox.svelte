<script>
    export let date;
    export let text;
    export let line = true;
</script>

<div class="timelineBox">
    <div class="middle">
        <h1>{date}</h1>
        <p>{text}</p>
    </div>
</div>
{#if line}
<div class="vl"></div>
{/if}