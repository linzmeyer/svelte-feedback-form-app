<script>
import FeedbackForm from "./components/FeedbackForm.svelte";

import FeedbackList from "./components/FeedbackList.svelte";
import FeedbackStats from "./components/FeedbackStats.svelte";

// moved to the store!
// this caused a lot of clean up in our code. Beatiful!
// let feedback = [
// 	{
// 		id: 1,
// 		rating: 10,
// 		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
// 	},
// 	{
// 		id: 2,
// 		rating: 9,
// 		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
// 	},
// 	{
// 		id: 3,
// 		rating: 8,
// 		text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
// 	},
// ];

// moved to FeedbackStats component
// $: count = feedback.length;
// $: average = feedback.reduce((a, {rating}) => a + rating, 0) / feedback.length;


// not needed anymore because of store
// const deleteFeedback = (e) => {
// 	const itemId = e.detail;
// 	feedback = feedback.filter((item) => item.id !== itemId);
// }

// const addFeedback = (e) => {
// 	console.log(e.detail);
// 	feedback = [e.detail, ...feedback];
// }

</script>

<main class="container">
	<!-- <FeedbackForm on:add-feedback={addFeedback} /> -->
	<!-- <FeedbackStats {count} {average} /> -->
	<!-- <FeedbackList on:delete-feedback={deleteFeedback} /> -->
	<FeedbackForm />
	<FeedbackStats />
	<FeedbackList />
</main>
