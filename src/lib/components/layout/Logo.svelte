<script>
  import overlay from '$lib/assets/static/logo/anim/overlay.png';
  import mask from '$lib/assets/static/logo/anim/mask.png';
  import bg from '$lib/assets/static/logo/anim/bg.png';
</script>

<div class="size-128 animate-[spin_120s_linear_infinite] select-none">
  <img class="absolute z-10 select-none" src={overlay} alt="" draggable="false" />
  <div
    class="mask-alpha mask-center mask-no-repeat select-none"
    style={`mask-image: url(${mask})`}
    draggable="false">
    <img
      class="animate-[reverse-spin_120s_linear_infinite] select-none"
      src={bg}
      alt=""
      draggable="false" />
  </div>
</div>
