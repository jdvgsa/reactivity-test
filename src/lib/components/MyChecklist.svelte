

<script>
  let myDailyTasks = [
    {task: "Study Javascript", editing: false, checked: true},
    {task: "Do Homework", editing: false, checked: false},
    {task: "Cook Dinner", editing: false, checked: true}
  ];   // this will be the initial array rendered of my daily tasks

  let textInput = "";

  function addDailyTasks() {
  myDailyTasks = [...myDailyTasks, { task: textInput, editing: false, checked: false }];
  }

  function setEditing(i, isEditing) {
    myDailyTasks[i].editing = isEditing; // True or False
  }

  function removeTasks(i) {
    myDailyTasks.splice(i, 1);
    myDailyTasks = myDailyTasks; // svelte is unaware of what splice does to array, this syntax allows myDailyTasks to be updated. 
  }
</script>
<section>
<div>
  <h3>Add Chores!</h3>
  <div>
    <input type="text" bind:value={textInput}>
    <button on:click={addDailyTasks}>Add</button>
  </div>
</div>

{#each myDailyTasks as tasks, i}

<div>
  {#if tasks.editing}
    <input type="text" bind:value={tasks.task}>
  {:else}
    <input type="checkbox" bind:checked={tasks.checked}>
    <p>{tasks.task}</p>
  {/if}
  <div>
    {#if tasks.editing}
    <button on:click={() => setEditing(i, false)}>Save</button>
    {:else}
    <button on:click={() => setEditing(i, true)}>Edit</button>
    {/if}
    <button on:click={() => removeTasks(i)}>Remove</button>
  </div>
</div>
{/each}
</section>

<style>
  :global(body) {
    background-color: antiquewhite; 
    margin: 0;
    padding: 0;
    
  }

  section {
    background-color: rosybrown;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    max-width: 400px;
    margin: auto;
    padding: 1rem;
  }

  div {
    margin-bottom: 10px;
  }

  h3 {
    color: black;
    text-align: center;
    padding-right: 1rem;
    font-size: 15px;
  }

  input[type="text"] {
    padding: 8px;
    margin-right: 8px;
  }

  button {
    padding: 0.5rem;
    cursor: pointer;
    background-color: royalblue;
    color: white;
    border: none;
    border-radius: 10px;
    margin: 0.25rem;
  }

  button:hover {
    background-color: rgba(15, 175, 31, 0.781)
  }

  input[type="checkbox"] {
    margin-right: 8px;
  }

  p {
    display: inline;
    margin: 0;
    padding-left: 4px;
  }

  div {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  
 
</style>