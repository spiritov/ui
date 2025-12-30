<script module>
  // @ts-nocheck

  import '../routes/layout.css';

  import { defineMeta } from '@storybook/addon-svelte-csf';

  import Table from '$lib/components/display/table/Table.svelte';
  import TablePlayer from '$lib/components/display/table/TablePlayer.svelte';
  import Division from '$lib/components/display/DivisionTag.svelte';
  import TableMap from '$lib/components/display/table/TableMap.svelte';

  const { Story } = defineMeta({
    component: Table
  });

  const data = [
    {
      country: 'United States',
      country_code: 'us',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaker',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Platinum',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 1
    },
    {
      country: 'United States',
      country_code: 'jp',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaking',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Diamond',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 2
    },
    {
      country: 'United States',
      country_code: 'nz',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambroken',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Wood',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 3
    },
    {
      country: 'United States',
      country_code: 'us',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaker',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Platinum',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 1
    },
    {
      country: 'United States',
      country_code: 'jp',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaking',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Diamond',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 2
    },
    {
      country: 'United States',
      country_code: 'nz',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambroken',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Wood',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 3
    },
    {
      country: 'United States',
      country_code: 'us',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaker',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Platinum',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 1
    },
    {
      country: 'United States',
      country_code: 'jp',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambreaking',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Diamond',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 2
    },
    {
      country: 'United States',
      country_code: 'nz',
      created_at: '1',
      demo_division: 'Wood',
      display_name: 'dreambroken',
      id: '1',
      preferred_class: 'Soldier',
      preferred_launcher: 'Stock',
      role: 'Admin',
      soldier_division: 'Wood',
      steam_avatar_url:
        'https://avatars.fastly.steamstatic.com/a601329884762a3ae565a8cf369ef9f4178b0daf_full.jpg',
      tempus_id: 3
    }
  ];
</script>

<Story name="Table" args={{}}>
  {#snippet template(args)}
    <Table {data}>
      {#snippet header()}
        <th class="w-1/12">id</th>
        <th class=""></th>
        <th class="w-1/4">map</th>
        <th class="w-1/12">division</th>
      {/snippet}
      {#snippet row(player)}
        <td>{player.id}</td>
        <td><TablePlayer {player} /></td>
        <td><TableMap map="jump_flood" /></td>
        <td><Division div={player.soldier_division} /></td>
      {/snippet}
    </Table>
  {/snippet}
</Story>
