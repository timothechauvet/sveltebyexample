<script>
    import Todo from "./Todo.svelte";
    let todos = [
        { task: "Mow lawn", completed: false },
        { task: "Garer le chien", completed: false },
        { task: "Promener la voiture", completed: false },
    ]
</script>

{#each todos as todo}
    <Todo {...todo} />
{/each}

{#if todos.length === 0}
  <p>All done!</p>
{:else if todos.length === 1}
  <p>Almost there!</p>
{:else}
  <p>Keep going!</p>
{/if}