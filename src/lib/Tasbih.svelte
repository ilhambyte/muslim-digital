<script>
  let count = 0;
  const increment = () => {
    count += 1;
  };
</script>

<h2>Tasbih Digital</h2>
<button on:click={increment}>
  Tasbih ke {count}
</button>

<style>
  button {
    color: #fff;
    background-color: blue;
    border-bottom: 5px solid #000;
    border-right: 4px solid #000;
  }
  button:hover {
    background-color: darkblue;
    border-bottom: 0 solid #000;
    border-right: 0 solid #000;
  }
</style>
