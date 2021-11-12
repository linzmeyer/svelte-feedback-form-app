<script>
// import { onDestroy, onMount } from 'svelte';
import { fade, scale, slide } from 'svelte/transition';
import { FeedbackStore } from '../stores';
import FeedbackItem from "./FeedbackItem.svelte";

// let feedback = [];

// const unsubscribe = FeedbackStore.subscribe((data) => feedback = data);

// onMount(() => {
//   console.log("component mounted.");
// })

// onDestroy(() => {
//   console.log("component destroyed.");
//   unsubscribe();
// })

</script>


<!-- {#each feedback as fb (fb.id)} -->
<!-- doing it with the store itself, will auto sub/unsubscribe for you so you don't need to do it mannually like above -->
{#each $FeedbackStore as fb (fb.id)}
<div in:fade out:slide="{{ duration: 1000 }}" >
  <!-- <FeedbackItem item={fb} on:delete-feedback /> don't need this event forwarder anymore -->
  <FeedbackItem item={fb} />
</div>
{/each}
