

<script>
   import { onMount } from 'svelte';
   let input = '';
   onMount(() => {
   const keyActions = {
    '1': function() {
      input = '1';
    },
    '2': function() {
      input = '2';
    },
    '3': function() {
      input = '3';
    },
    '4': function() {
      input = '4';
    },
  };


fetch('moveSet_test.json')
  .then(response => response.json())
  .then(data => {
    // Accessing the questions array
    // console.log(data.questions);

    // Accessing a specific question and its options
    // console.log(data.questions[0].question);
    // console.log(data.questions[0].options);
    console.log(data.questions[1].options[0]);

    // Accessing the correct answer index for a specific question
    // console.log(data.questions[1].answer);
  })
  .catch(error => console.error(error));

  // @ts-ignore
  function handleKeyDown(event) {
    const key = event.key.toLowerCase();
  
    if (key in keyActions) {
      // @ts-ignore
      keyActions[key]();
    }
  }
  
  document.addEventListener("keydown", handleKeyDown, false);
});




function loadQuestion(){
	// Fetch the JSON file
	fetch('questions.json')
	.then(response => response.json())
	.then(data => {
		// Get a random question index
		const randomIndex = Math.floor(Math.random() * data.questions.length);

		// Access the random question and its options
		const randomQuestion = data.questions[randomIndex];
		console.log(randomQuestion.question);
		console.log(randomQuestion.options);
	})
	.catch(error => console.error(error));  

}




</script>


<h1>move! </h1>
<div class="fixed h-screen bg-white inset-0 ">
<input bind:value={input} placeholder="testing box" />
  <div class="flex items-center justify-center">
    <div class="h1">Hi!</div>
    <div class="grid grid-cols-1">
      <div class="bg-gray-300 p-20 m-20">Box 1</div>
      <div class="bg-gray-300 p-20 m-20">Box 3</div>
    </div>
    <div class="h1">move!   |   {input || ' loading... '}   |   move!</div>
    <div class="grid grid-cols-1">
      <div class="bg-gray-300 p-20 m-20">Box 2</div>
      <div class="bg-gray-300 p-20 m-20">Box 4</div>
    </div>
  </div>
</div>



<h1 class="text-3xl font-bold underline">
</h1>
<br>
<br>
