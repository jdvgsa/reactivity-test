<script>
  import MyChecklist from "../lib/components/MyChecklist.svelte"
  import Reset from "../lib/components/Reset.svelte";
</script>

<h1>Assignment 6</h1>
<h2>My Svelte Checklist App</h2>

<div>
<MyChecklist />
</div>

<div>
  <Reset />
</div>

<p><br></p>

<footer>
  <p>&copy; 2023 John Dagsa 262 Svelte Assignment</p>
</footer>


<style>
  
  h1 {
    display: flex;
    justify-content: center;
    padding: 0 auto;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }

  h2 {
    display:flex;
    justify-content: center;
    padding: 0.5rem;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
    
  footer {
    background-color: grey;
    text-align: center;
    padding: 10px;
    color: black;
    font-weight: bolder;
  }
</style>
