<script>
  // import MyArrayComponent from "../lib/components/MyArrayComponent.svelte";
  // import myDailies from "..lib/data.js";

  // declaring daily tasks array
  let dailyTasks = [
    {task: "Exercise"},
    {task: "Buy Groceries"},
    {task: "Walk Dog"},
  ];
  
</script>

<h1>Reactivity and Events</h1>
<h2><strong>Daily Tasks123</strong></h2>
<!-- rendering daily tasks array -->
<main>
  {#each dailyTasks as tasks}
    <ul>
      <li>{tasks.task}</li>
    </ul>
  {/each}
</main>







<style>
  h1 {
    display: flex;
    justify-content: center;
  }
</style>
<!-- <span>
  <MyArrayComponent {...MyArrayComponent} />
</span> -->