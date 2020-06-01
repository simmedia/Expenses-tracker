<script>
  import { slide } from "svelte/transition";
  export let transaction;
  export let removeTransaction;
</script>

<div
  transition:slide
  class="notification is-light {transaction.value > 0 ? 'is-success' : 'is-danger'}">
  {transaction.value}
  <button class="delete" on:click={() => removeTransaction(transaction._id)} />
</div>
