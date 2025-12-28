<script lang="ts">
  type Props = {
    src: string;
    href: string;
    label: string;
  };

  let { src, href, label }: Props = $props();
</script>

<a class="flex w-fit gap-1 text-primary/75 hover:text-primary hover:underline" {href}>
  <img class="size-6" {src} alt="" />
  <span>{label}</span>
</a>
