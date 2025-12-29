<script lang="ts">
  type Props = {
    points: ClassPoints;
  };

  let { points }: Props = $props();
</script>

<div class="flex gap-2">
  {@render category('last 3 monthly', points.last_3_monthly)}
  {@render category('last 9 motw', points.last_9_motw)}
  {@render category('total', points.total)}
</div>

{#snippet category(label: string, value: number)}
  <div class="flex h-fit min-w-24 flex-col bg-base-700/0">
    <span class="text-sm text-content/75">{label}</span>
    <span>{value}</span>
  </div>
{/snippet}
