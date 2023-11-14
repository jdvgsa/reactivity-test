<script>
  import MyChecklist from "../lib/components/MyChecklist.svelte"

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

<div class="container">
  to do app
</div>

<MyChecklist />





<style>
  h1 {
    display: flex;
    justify-content: center;
  }

  .container {
    width: 750px;
    background-color: cyan;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-align: center;
  }
</style>




<!-- <span>
  <MyArrayComponent {...MyArrayComponent} />
</span> -->