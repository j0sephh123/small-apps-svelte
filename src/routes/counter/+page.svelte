<script>
  let count = 0;
  $: className = count === 0 ? 'counter' : (count > 0 ? "counter success" : "counter failure");

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

<div class="app">
  <div class="content">
    <button class="button" on:click={handleDecrement}>-</button>
    <div class={className} id="counter">{count}</div>
    <button class="button" on:click={handleIncrement}>+</button>
  </div>
  <button class="button" on:click={handleReset}>Reset</button>
</div>
