<script>
  import Tasbih from "./lib/Tasbih.svelte";
  import Hafalan from "./lib/Hafalan.svelte";
</script>

<main>
  <h1>🕋 Muslim Digital</h1>
  <div class="card">
    <Tasbih />
    <Hafalan />
  </div>
</main>

<style>
  .card {
    background-color: aquamarine;
    border-radius: 14px;
  }
  ::selection {
    color: chartreuse;
  }
</style>
