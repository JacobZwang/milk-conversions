<script>
  import InputMilkType from "./InputMilkType.svelte";

  let iHave1 = "whole milk";
  let iHave2 = "whipping cream";

  function handleIHave1(event) {
    iHave1 = event.detail;
  }

  function handleIHave2(event) {
    iHave2 = event.detail;
  }
</script>

<p>
  I have
  <InputMilkType on:handleInput={handleIHave1} defaultSelected={iHave2} />
  and
  <InputMilkType on:handleInput={handleIHave2} defaultSelected={iHave2} />
</p>
{iHave1}<br />{iHave2}
