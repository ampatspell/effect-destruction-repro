<script lang="ts">
	import { goto } from "$app/navigation";

  $effect(() => {
    console.log('create');
    return () => {
      console.log('destroy');
    }
  });
</script>

<div class="page">
  <div class="row">/dev/thing</div>
  <div class="row"><a href="/">back to index</a></div>
</div>
