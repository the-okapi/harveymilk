<script>
    import TopBar from '$lib/TopBar.svelte';
    import harvey from '$lib/assets/harvey.png';
    import BottomBar from '$lib/BottomBar.svelte';
</script>

<TopBar />

<div class="aboutContainer">
    <div class="aboutText">
            <h1 class="aboutName"><span class="red">Ha</span><span class="orange">rv</span><span class="yellow">ey</span> <span class="green">Mi</span><span class="blue">lk</span></h1>
            <p><span class="bold">Born:</span> May 22, 1930 in Woodmere, NY, US</p>
            <p><span class="bold">Died:</span> November 27, 1978 in San Francisco, CA, US</p>
            <p><span class="bold">Parents:</span> William Milk and Minerva Karns Milk</p>
            <p>Member of the San Francisco Board of supervisors</p>
            <p>Served in the US Navy as a diving officer</p>
            <p>Recipient of the Presidential Medal of Freedom</p>
    </div>
    <img alt='Harvey Milk' src={harvey} class='aboutImage'>
</div>

<BottomBar />