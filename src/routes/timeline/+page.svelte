<script>
    import TopBar from '$lib/TopBar.svelte';
    import BottomBar from '$lib/BottomBar.svelte';
    import TimelineBox from '$lib/TimelineBox.svelte';
</script>

<TopBar />
<div class="timelineContainer">
    <TimelineBox date={'May 22, 1930'} text={'Harvey Bernard Milk, a lithuanian jewish boy is born'}/>
    <TimelineBox date={'1943 - 1947'} text={'Harvey attends Bay Shore High School'}/>
    <TimelineBox date={'1947 - 1951'} text={'Harvey goes to New York State College for Teachers'}/>
    <TimelineBox date={'1951 - 1955'} text={'Harvey serves in the navy as a diver on the USS Kitiwake'}/>
    <TimelineBox date={'1956'} text={'Harvey meets Joe Campbell. They will be together for six years'}/>
    <TimelineBox date={'1956 - 1961'} text={'Harvey is a teacher and basketball coach at a New York High School'}/>
    <TimelineBox date={'1962'} text={'Harvey\'s Mother Minerva Dies'}/>
    <TimelineBox date={'1972'} text={'Harvey and his new boyfriend Scott Milk move to San Francisco'}/>
    <TimelineBox date={'1973'} text={"Harvey and Scott open Castro Camera"}/>
    <TimelineBox date={'November, 1973'} text={'Harvey runs for the San Francisco Board of Supervisors representing District 5, he does not win'}/>
    <TimelineBox date={'November, 1975'} text={'Harvey runs for the Board of Supervisors and loses again'}/>
    <TimelineBox date={'1976'} text={'Harvey gets named to the Board of Permit Appeals'}/>
    <TimelineBox date={'November 8, 1977'} text={'Harvey gets elected to the Board of Supervisors. He becomes the first openly gay man elected to a political position in the US'}/>
    <TimelineBox date={'June 25, 1978'} text={'Harvey gives what is now called the \'Hope\' speech'}/>
    <TimelineBox date={'November, 1978'} text={'Harvey defeats a bill to get all gay teachers in San Francisco fired'}/>
    <TimelineBox date={'November 27, 1978'} text={'Dan White assasinates Harvey Milk and Mayor George Moscone at City Hall'} line={false} />
</div>

<BottomBar />