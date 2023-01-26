<template>
  <div class="w-screen h-screen flex">
    <!--Side bar-->
  <div class="w-[400px] h-full bg-gray-200 text-white" v-show="showSide">
  <div class="h-[50px] bg-gray-900 flex justify-start items-center">
<div class="px-[20px]">
  <h3 class="font-bold text-xl">Admin Dashboard</h3>
</div>
  </div>
  <div class="h-[calc(100vh-50px)] bg-gray-800 py-[20px]">
    <div class="flex flex-col justify-between h-full px-[20px] space-y-[10px]">

    
    <div class="flex flex-col justify-between space-y-[10px]">
      <router-link to="/home" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-sm font-medium rounded-md border-gray-200 hover:bg-gray-200 hover:text-gray-200">
        <svg aria hidden="true" class="mr-2 w-[25px] h-[25px] fill-current" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M18 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.08"></path>
        </svg>
        Home
      </router-link>

      <router-link to="/profile" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-sm font-medium rounded-md border-gray-200 hover:bg-gray-200 hover:text-gray-200">
        <svg aria hidden="true" class="mr-2 w-[25px] h-[25px] fill-current" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M18 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.08"></path>
        </svg>
        Profile
      </router-link>

      <router-link to="/messages" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-sm font-medium rounded-md border-gray-200 hover:bg-gray-200 hover:text-gray-200">
        <svg aria hidden="true" class="mr-2 w-[25px] h-[25px] fill-current" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M18 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.08"></path>
        </svg>
        Messages
      </router-link>

      <router-link to="/download" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-sm font-medium rounded-md border-gray-200 hover:bg-gray-200 hover:text-gray-200">
        <svg aria hidden="true" class="mr-2 w-[25px] h-[25px] fill-current" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M18 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.08"></path>
        </svg>
        Download
      </router-link>
    
      </div>
      <div class="h-[50px]">
      <div>
        <router-link to="/setting" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-sm font-medium rounded-md border-gray-200 hover:bg-gray-300 hover:text-sm">
          <svg aria-hidden="true" class="mr-2 w-[25px] h-[25px] fill-current" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
      <path fill-rule="evenodd" d="M18 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.08"></path>
          </svg>
        Setting
        </router-link>
      </div>
     <div>

     </div>
    </div>
  </div>
  </div>
  </div>
  <div class="w-full h-full bg-gray-400">
  <div class="h-[50px] bg-gray-100 flex items-center shadow-sm px-[20px] w-full py-[10px] z-10 border-b">
  <!--Hamburger Menu-->
  <div class="cursor-pointer w-[10px]" @click="toggleSideBar">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="w-[25px]">
    <path d="M0 96CO 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 9"></path>
  </svg>
  </div>
<!--Search bar-->
<div class="w-[calc(100%-30px)] flex">
<div class="w-[calc(100%-200px)] flex justify-center">
  <!--Search bar-->
<form class="flex items-center x-[500px]">
  <label for="voice-search" class="sr-only">Search</label>
<div class="relative w-full">
  <div class="flex absolute inset-y-0 left-0 items-center pt-3 pointer-events-none">
    <svg aria-hidden="true" class="w-5 auto text-gray-500 dark:text-gray-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
      <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.47614.817a1 1 0 01-1.414 1.4141-4.8"></path>
    </svg>
  </div>
  <input type="text" id="voice-search" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-bl"/>
  <router-link to="/" class="flex absolute inset-y-0 right-0 items-center pr-3">
    <svg aria-hidden="true" class="w-4 h-4 text-gray-500 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white" fill="">
      <path fill-rule="evenodd" d="M7 4a3 3 0 016 0v4a3 3 0 11-6 0v4zm4 10.9347.001 0 0017 8al 1 0 10-2 0A5 5 0 015 8a1"></path>
    </svg>
  </router-link>
</div>
</form>
</div>
<!--User Login -->
<div class="w-[200px]">
  <div class="flex items-center justify-start space-x-4" @click="toggleDrop">
    <img class="w-10 h-10 rounded-full border-gray-50" src="https://yt3.ggpht.com/hqsxh-ynbw90K0.X40AWh68kmEUVnl -82SRCyh-">
    <div class="font-semibold dark:text-white text-left">
      <div>Joe App</div>
      <div class="text-xs text-gray-500 dark:text-gray-400">Admin</div>
    </div>
  </div>
  <!--Drop down-->
  <div v-show="showDropDown" class="absolute right-[10px] z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1">
  <div class="py-1 text-left" role="none">

    <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-0">Account Settings</a>
    <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-0">Support</a>
    <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-0">License</a>
  <form method="POST" action="#" role="none">
    <button type="submit" class="text-gray-700 block w-full px-4 py-2 text-left text-sm" role="menuitem" tabindex="-1"></button>
  </form>
  </div>
  </div>
</div>
</div>
  </div>
  <div class="h-[calc(100vh-50px)] bg-gray-50 p-[20px]">
    <div class="border border-gray-300 rounded-md p-[20px] h-full">
<router-view></router-view>
    </div>
  </div>
  </div>
  <!--Main-->
  </div>
  </template>
  
  <script>
  export default {
    data(){
      return {
        showDropDown:false,
        showSide:true
      }
    },
  methods:{
    // hide show side bar
    toggleSideBar(){
      this.showSide = !this.showSide
    },
    // toggle user
    toggleDrop(){
    this.showDropDown = !this.showDropDown
    },
  }
  }
  </script>
  
  <style>
  
  </style>