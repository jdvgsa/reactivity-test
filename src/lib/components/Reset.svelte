<script>
  function resetTask() {
    location.reload();
  }
</script>

<style>
  h2 {
    display: flex;
    justify-content: center;
  }

  .reset {
    display: flex;
    justify-content: center;
  }

  p {
    display: flex;
    justify-content: center;
  }
</style>

<h2>Reset Task App Button</h2>
<p>If you've added too many tasks and don't want to remove them one by one press this button to restart from the beginning.</p>
<div class="reset">
<button on:click={resetTask}>Reset Tasks</button>
</div>