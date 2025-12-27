<script module>
  import '../routes/layout.css';

  import { defineMeta } from '@storybook/addon-svelte-csf';

  import Flag from '$lib/components/display/Flag.svelte';

  const { Story } = defineMeta({
    component: Flag
  });
</script>

<Story name="Flag" args={{ code: 'us' }}></Story>
