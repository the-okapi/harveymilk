<script>
    import TopBar from '$lib/TopBar.svelte';
    import BottomBar from '$lib/BottomBar.svelte';
    import stamp from '$lib/assets/postageStamp.png';
    import young from '$lib/assets/youngHarvey.png';
    import beer from '$lib/assets/coors.png';
</script>

<TopBar />

<div class="accifContainer">
    <div class="accifRow">
        <div class="accifText">
            <p>Harvey was given the Presidential Medal of Freedom posthumously</p>
            <p>Harvey served in the navy during the Korean War</p>
            <p>Harvey was against the Vietnam War</p>
            <p>Harvey has his own day: Harvey Milk Day on May 22<sup>nd</sup></p>
            <p>There is a US postage stamp with Harvey's face on it</p>
        </div>
        <img class="accifImage" alt="Harvey Milk Postage Stamp" src={stamp}>
    </div>
    <div class="accifRow">
        <img class="accifImage" alt="Young Harvey Milk" src={young}>
        <div class="accifText">
            <p>Harvey's grandfather owned a department store</p>
            <p>Harvey was teased for his big ears, big nose and big feet as a kid</p>
            <p>Harvey was a class clown in school</p>
            <p>Harvey liked opera and football</p>
            <p>Harvey got a teaching degree</p>
        </div>
    </div>
    <div class="accifRow">
        <div class="accifText">
            <p>Harvey was once a stock analyst</p>
            <p>Harvey was an associate producer for a few movies</p>
            <p>Harvey lived in San Francisco, Texas and New York</p>
            <p>Harvey used to have long hair</p>
            <p>Harvey helped with a beer boycott</p>
        </div>
        <img class="accifImage" alt="Beer" src={beer}>
    </div>
</div>

<BottomBar />