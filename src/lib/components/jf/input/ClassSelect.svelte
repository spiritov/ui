<script lang="ts">
  import demo from '$lib/assets/tf/demo.png';
  import soldier from '$lib/assets/tf/soldier.png';

  type Props = {
    selected: string;
    onsubmit: (value: string) => void;
  };

  let { selected, onsubmit }: Props = $props();
</script>

<!-- bring your own container -->

<!-- soldier -->
<button
  class="cursor-pointer p-2 transition-opacity
  {selected === 'Demo' ? 'opacity-25 hover:opacity-75' : ''}"
  onclick={() => {
    onsubmit('Soldier');
    selected = 'Soldier';
  }}>
  <img class="max-w-16 object-cover" src={soldier} alt="" />
</button>
<!-- demo -->
<button
  class="cursor-pointer p-2 transition-opacity
  {selected === 'Soldier' ? 'opacity-25 hover:opacity-75' : ''}"
  onclick={() => {
    onsubmit('Demo');
    selected = 'Demo';
  }}>
  <img class="max-w-16 object-cover" src={demo} alt="" />
</button>

<style>
  /* match theme content color */
  img {
    filter: brightness(0) saturate(100%) invert(97%) sepia(49%) saturate(6023%) hue-rotate(179deg)
      brightness(100%) contrast(108%);
  }
</style>
