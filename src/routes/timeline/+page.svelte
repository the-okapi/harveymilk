<script>
    import TopBar from '$lib/TopBar.svelte';
    import BottomBar from '$lib/BottomBar.svelte';
    import TimelineBox from '$lib/TimelineBox.svelte';
</script>

<TopBar />
<div class="timelineContainer">
    <TimelineBox date={'May 22, 1930'} text={'Harvey Milk is born'} line={true} />
    <TimelineBox date={'1943 - 1947'} text={'Harvey attends Bay Shore High School'} line={true} />
    <TimelineBox date={'1947 - 1951'} text={'Harvey goes to New York Teachers College in Albany'} line={true} />
    <TimelineBox date={'1951 - 1955'} text={'Harvey serves in the navy as a diver on the USS Kitiwake'} line={true} />
    <TimelineBox date={'1956'} text={'Harvey meets Joe Campbell. They will be together for six years'} line={true} />
    <TimelineBox date={'1956 - 1961'} text={'Harvey is a teacher and basketball coach at a New York High School'} line={true} />
    <TimelineBox date={'1970'} text={'Harvey opens up about his sexuality'} line={true} />
    <TimelineBox date={'1972'} text={'Harvey and his new boyfriend move to San Francisco'} line={true} />
    <TimelineBox date={'November, 1973'} text={'Harvey runs for the San Francisco Board of Supervisors, he does not win'} line={true} />
    <TimelineBox date={'November 8, 1977'} text={'Harvey gets elected to the Board of Supervisors. He becomes the first openly gay man elected to a political position in the US'} line={true} />
    <TimelineBox date={'November, 1978'} text={'Harvey defeats a bill to get all gay teachers in San Francisco fired'} line={true} />
    <TimelineBox date={'November 27, 1978'} text={'Dan White assasinates Harvey Milk and Mayor George Moscone at City Hall'} line={false} />
</div>

<BottomBar />