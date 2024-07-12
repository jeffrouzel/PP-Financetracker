<template>
  <div class="w-screen h-screen flex flex-col">
    <!-- Navigation bar -->
    <NavigationBar />
    <div class="h-[calc(100vh-80px)] flex">
      <!-- Sidebar -->
      <Sidebar />
      <div class="w-screen h-screen px-24 py-16"><slot /></div>
    </div>
  </div>
</template>