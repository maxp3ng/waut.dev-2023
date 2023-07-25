<script>
  let name = '';
</script>

<div class="inset-y-1/2	p-6 mx-auto bg-white rounded-xl absolute z-0">
      <p class="text-slate-500">{name || "Enter text..."}</p>
</div>



    <!-- text box -->
  <div class="text-input flex mx-auto bg-slate-100">
    <input bind:value={name} placeholder="Type here..." />
  </div>


