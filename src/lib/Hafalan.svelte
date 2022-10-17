<script>
    let todos = [
        { done: false, text: "Surat Al-Baqarah" },
        { done: false, text: "Surat Ar-Rahman" },
        { done: false, text: "Surat Al-Kahfi" },
    ];

    function add() {
        todos = todos.concat({ done: false, text: "" });
    }

    function clear() {
        todos = todos.filter((t) => !t.done);
    }

    $: remaining = todos.filter((t) => !t.done).length;
</script>

<h2>Hafalan Surat</h2>

{#each todos as todo}
    <div class:done={todo.done}>
        <input type="checkbox" bind:checked={todo.done} />

        <input placeholder="Tulis surat disini.." bind:value={todo.text} />
    </div>
{/each}

<p>{remaining} surat tersisa</p>

<button on:click={add}> Tambahkan </button>

<button on:click={clear}> Bersihkan yang selesai</button>

<style>
    .done {
        opacity: 0.4;
    }
    ::selection{
        color: chartreuse;
    }
</style>
