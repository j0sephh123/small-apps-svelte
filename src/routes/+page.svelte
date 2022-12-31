<script>
  let count = 0;
  $: className = count === 0 ? null : (count > 0 ? "success" : "failure");

  function handleDecrement() {
    count -= 1;
  }
  function handleIncrement() {
    count += 1;
  }
  function handleReset() {
    count = 0;
  }
</script>

<div id="app">
  <div class="content">
    <button on:click={handleDecrement}>-</button>
    <div class={className} id="counter">{count}</div>
    <button on:click={handleIncrement}>+</button>
  </div>
  <button on:click={handleReset}>Reset</button>
</div>
