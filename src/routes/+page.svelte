<script>
  let count = 0;

  const increment = () => count++;
  const decrement = () => count > 0 && count--;
  const reset = () => count = 0;
</script>

<style>
    .counter-color{
        color: orange;
        font-weight: 900;
        font-size: 150px;
    }
</style>
<div class="row justify-content-center mt-5">
  <div class="col-md-8 text-center">
    <h3 class="fw-bold mb-4">
      <span class="display-4 counter-color">{count}</span>
    </h3>

    <div class="d-flex justify-content-center gap-2">
      <button class="btn btn-success" on:click={increment}>
        <i class="bi bi-plus-circle"></i> Aumentar
      </button>

      <button
        class="btn btn-danger"
        on:click={decrement}
        disabled={count === 0}
        aria-disabled={count === 0}
      >
        <i class="bi bi-dash-circle"></i> Disminuir
      </button>

      <button
        class="btn btn-primary"
        on:click={reset}
        disabled={count === 0}
        aria-disabled={count === 0}
      >
        <i class="bi bi-arrow-counterclockwise"></i> Resetear
      </button>
    </div>
  </div>
</div>
