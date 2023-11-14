<!-- <svelte:head>
  <script src="htpps://cdn.tailwindcss.com"></script>
</svelte:head> -->

<script>
  let myDailyTasks = [
    // {task: "Study Javascript", editing: false, checked: true},
    // {task: "Do Homework", editing: false, checked: false},
    // {task: "Cook Dinner", editing: false, checked: false},
  ];   // this will be the array of my daily tasks

  let textInput = " ";

  function addDailyTasks() {
  myDailyTasks = [...myDailyTasks, { task: textInput, editing: false, checked: false }]
  }

  function setEditing(i, isEditing) {
    myDailyTasks[i].editing = isEditing; // True or False
  }

  function removeTasks(i) {
    myDailyTasks.splice(i, 1);
    myDailyTasks = myDailyTasks; // svelte is unaware of what splice does to array, this syntax allows myDailyTasks to be updated. 
  }
</script>

<div>
  <h3>My Svelte Checklist Application</h3>
  <div>
    <input type="text" bind:value={textInput}>
    <button on:click={addDailyTasks}>Add</button>
  </div>
</div>

{#each myDailyTasks as tasks, i}

<div>
  {#if tasks.editing}
    <input type="text" bind:value={tasks.content}>
  {:else}
  <input type="checkbox" bind:checked={tasks.checked}>
  <h4>{tasks.content}</h4>
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

<style>
  input {
    display: flex;
    padding: 1rem;
    margin-right: 8px;
    border: none;
    background-color: antiquewhite;
    text-align: center;
  }

  button {
    padding: 0.5rem;
  }
 
</style>