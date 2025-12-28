<script lang="ts">
  import Flag from '../Flag.svelte';

  type Props = {
    player: Player;
  };

  let { player }: Props = $props();
</script>

<div class="flex size-full cursor-pointer items-center gap-1">
  <Flag code={player.country_code} />
  <img class="ml-3 size-8 rounded-box" src={player.steam_avatar_url} alt="" />
  <span class="truncate hover:underline">{player.display_name}</span>
</div>
