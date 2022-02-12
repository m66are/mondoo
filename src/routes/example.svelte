<script>
let todos = [];
let todoText ='';
function addTodo (){
    todos = [...todos,todoText];
};
function clearList(){
    todos = [];
}


</script>

<main>
    <!-- todos list -->
    {#if todos.length > 0 }
    <div>
<div><h2>MY LIST </h2> </div>


<div>
    {#each todos as toot}
    <div>{toot}</div>
        
    {/each}
</div>
<button on:click|preventDefault={clearList}>Clear liiiiist</button>
</div>
{:else}
<h2>Your list is empty</h2>
{/if}

  <!-- todos list -->
<form on:submit|preventDefault={addTodo}>


    <input type="text" name="" id="" bind:value={todoText}>
    <input type="submit" value="Submit">
</form>


</main>

<style>

</style>