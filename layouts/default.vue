<template>
  <div class="w-screen h-screen flex flex-col">
    <!-- Navigation bar -->
    <NavigationBar />
    <div class="h-[calc(100vh-50px)] flex">
      <!-- Sidebar -->
      <Sidebar />
      <div class="size-4/6 px-6 py-8"><slot /></div> 
      <Inputmoney />
    </div>
  </div>
</template> 