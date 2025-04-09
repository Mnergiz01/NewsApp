<template>
    <div class="flex flex-row gap-3 items-start pb-3 border-b border-gray-300">
      <!-- Küçük Görsel -->
      <div class="flex-shrink-0">
        <img
          src="@/assets/Rectangle 24.png"
          alt="News Image"
          class="w-20 h-20 object-cover rounded-md shadow-sm"
        />
      </div>
  
      <!-- Küçük Metin -->
      <div class="flex flex-col space-y-1">
        <h1 class="text-xs font-semibold text-gray-900 leading-tight">
          U.S. downs suspected Chinese spy balloon over the Atlantic coast
        </h1>
        <p class="text-[9px] text-gray-600 leading-tight">
          China called the vessel’s downing “an excessive reaction” and said it “retains the right to respond further.”
        </p>
        <div class="flex justify-between items-center text-[9px] text-gray-500">
          <p>By <span class="text-blue-500 hover:underline cursor-pointer">John Doe</span></p>
          <p>Feb 4, 2023</p>
        </div>
      </div>
    </div>
  </template>
  