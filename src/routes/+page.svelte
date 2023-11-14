<script>
  import MyChecklist from "../lib/components/MyChecklist.svelte"

  // declaring daily tasks array (redundant code)
  // let dailyTasks = [
  //   {task: "Exercise"},
  //   {task: "Buy Groceries"},
  //   {task: "Walk Dog"},
  // ];
  
</script>

<h1>Reactivity and Events</h1>


<!-- <h2><strong>Daily Tasks123</strong></h2>
rendering daily tasks array
<main>
  {#each dailyTasks as tasks}
    <ul>
      <li>{tasks.task}</li>
    </ul>
  {/each}
</main> -->


<div class="app">
<MyChecklist />
</div>





<style>
  h1 {
    display: flex;
    justify-content: center;
  }

  .app {
    display: flex;
    justify-content: space-evenly;
  }

  
</style>




<!-- <span>
  <MyArrayComponent {...MyArrayComponent} />
</span> -->