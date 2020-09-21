<script>
  export let defaultSelected;
  let selected = defaultSelected;

  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  function test() {
    dispatch("handleInput", selected);
  }
</script>

<select bind:value={selected} on:change={test}>
  <option value="heavy whipping cream">heavy whipping cream</option>
  <option value="whipping cream">whipping cream</option>
  <option value="half and half">half and half</option>
  <option value="whole milk">whole milk</option>
  <option value="lowfat milk">lowfat milk</option>
  <option value="nonfat/skim milk">nonfat/skim milk</option>
</select>
