<script>
	let newTodo = ''
	let todos  =[]

let newId = 0
let count = 0

const addTodo =()=>{
	newId++
	todos  = [...todos,{text:newTodo,id:newId}]
	newTodo = ''
}





</script>



<main>
	<h1>My first TODO app in SVELTE</h1>
	
	<input type="text" placeholder="New todo" bind:value={newTodo} >
	<button on:click={addTodo} >Add todo</button>
{#if todos.length>0 }

{#each todos as todo (todo.id) }
	<h2>{todo.text}  </h2>
	
	<!-- <button  >Delete</button> -->
{/each}

{:else}
	<h3>There are no Todo</h3>
{/if}

</main>
<style>

</style>