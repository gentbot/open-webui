<script lang="ts">
  // the speed of the spoken content
  const instanceName = `range-${Math.random().toString(32)}`;
	export let rangeValue = 1;
	export let minValue = 0;
	export let maxValue = 3;
	export let stepValue = 0.1;
  export let showValue = true;
</script>

<!-- <style>
  :root {
  --track-bg-light: #ddd;
  --thumb-bg-light: #007aff;
  --track-bg-dark: #444;
  --thumb-bg-dark: #1e90ff;
}

@media (prefers-color-scheme: dark) {
  :root {
    --track-bg: var(--track-bg-dark);
    --thumb-bg: var(--thumb-bg-dark);
  }
}

@media (prefers-color-scheme: light) {
  :root {
    --track-bg: var(--track-bg-light);
    --thumb-bg: var(--thumb-bg-light);
  }
}

/* General styles for the range input */
input[type="range"] {
  -webkit-appearance: none;
  width: 100%;
  height: 8px;
  background: transparent;
}

/* WebKit browsers */
input[type="range"]::-webkit-slider-runnable-track {
  height: 8px;
  background: var(--track-bg);
  border-radius: 4px;
}
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 20px;
  height: 20px;
  background: var(--thumb-bg);
  border-radius: 50%;
  cursor: pointer;
}

/* Mozilla browsers */
input[type="range"]::-moz-range-track {
  height: 8px;
  background: var(--track-bg);
  border-radius: 4px;
}
input[type="range"]::-moz-range-thumb {
  width: 20px;
  height: 20px;
  background: var(--thumb-bg);
  border-radius: 50%;
  cursor: pointer;
}

/* MS Edge */
input[type="range"]::-ms-track {
  height: 8px;
  background: transparent;
  border-color: transparent;
  color: transparent;
}
input[type="range"]::-ms-fill-lower,
input[type="range"]::-ms-fill-upper {
  background: var(--track-bg);
  border-radius: 4px;
}
input[type="range"]::-ms-thumb {
  width: 20px;
  height: 20px;
  background: var(--thumb-bg);
  border-radius: 50%;
  cursor: pointer;
}

</style> -->

<div class="flex items-center justify-between">

  <input
    type="range"
    class="mx-1.5"
    name="{instanceName}"
    min="{minValue}"
    max="{maxValue}"
    step="{stepValue}"
    bind:value="{rangeValue}"
  />
  {#if showValue}
  <label for={instanceName}>{rangeValue.toFixed(1)}</label>
  {/if}
</div>
