<script lang="ts">
  type Props = {
    label: string;
    options: {
      src: string;
      value: string;
    }[];
    withNone?: boolean;
    selected: string;
    onsubmit: (value: string) => void;
  };

  let { label, options, withNone = false, selected, onsubmit }: Props = $props();

  $inspect(selected);
</script>

<!-- container for input -->
<label
  class="relative mt-2 flex w-fit rounded-box border border-base-700 bg-base-800 transition-colors focus-within:border-content/50 hover:border-content/50">
  <!-- label -->
  <span class="absolute -top-1 left-2 bg-base-800 px-1 text-sm leading-1">{label}</span>
  <!-- input container -->
  <div class="flex h-18 w-full">
    {#each options as { value, src }}
      {@const isSelected: boolean = selected === value}
      <button
        class="rounded-box {isSelected ? 'bg-base-900' : 'bg-base-800'}"
        onclick={() => {
          onsubmit(value);
          selected = value;
        }}>
        <img class="w-20 px-2" {src} alt="" draggable="false" />
      </button>
    {/each}
    <!-- reset option -->
    {#if withNone}
      {@const noneSelected: boolean = selected === 'None'}
      <!-- svelte-ignore a11y_consider_explicit_label -->
      <button
        class="grid w-20 place-content-center rounded-box {noneSelected
          ? 'bg-base-900'
          : 'bg-base-800'}"
        onclick={() => {
          onsubmit('None');
          selected = 'None';
        }}>
        <span class="icon-[mdi--close] size-6"></span>
      </button>
    {/if}
  </div>
</label>
