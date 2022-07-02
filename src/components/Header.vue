<script setup lang="ts">
import { reactive } from 'vue'
const { t } = useI18n();

const state = reactive({
  openMenu: false
})
</script>

<template>
  {{ n2 }}
  <header class="shadow-sm py-3">
		<div class="container max-w-screen-xl mx-auto px-4">
			<div class="flex flex-wrap items-center">
				<!-- Brand -->
				<div class="flex-shrink-0 mr-5">
          <RouterLink class="icon-btn mx-2" to="/" title="Brand E-commerce">
             <img src="./../assets/logo.svg" height="38">
          </RouterLink>
				</div>
				<!-- Brand .//end -->
				
				<!-- Search -->
				<div class="flex flex-nowrap items-center w-full order-last md:order-none mt-5 md:mt-0 md:w-1./4 lg:w-1.5/4">
					<input class="flex-grow appearance-none border border-gray-200 bg-gray-100 rounded-md mr-2 py-2 px-3 hover:border-gray-400 focus:outline-none focus:border-gray-400" type="text" placeholder="Search">
					<button type="button" class="px-4 py-2 inline-block border border-transparent bg-blue-600 rounded-md hover:bg-blue-700">
            <div i-carbon-search class="text-gray-100" />
					</button>
				</div>
				<!-- Search .//end -->

				<!-- Actions -->
				<div class="flex items-center space-x-2 ml-auto">

          <HeaderButton title="Sign In" icon="carbon-user" />
          
          <HeaderButton title="Whitelist" icon="carbon-favorite" />

          <HeaderButton title="My cart" icon="carbon-shopping-cart" />
     
          <button class="px-1 py-2 inline-block text-center flex items-center !outline-none" :title="t('button.toggle_dark')" @click="toggleDark()">
            <div i="carbon-sun dark:carbon-moon" />
          </button>

				</div>
				<!-- Actions .//end -->
				
				<!-- mobile-only -->
				<div class="lg:hidden ml-2">
					<button type="button" @click="state.openMenu = !state.openMenu" class="p-3 inline-flex items-center rounded-md text-black hover:bg-gray-200 hover:text-gray-800 border border-transparent">
						<span class="sr-only">Open menu</span>
						<div i="carbon-menu" />
					</button>
				</div>
				<!-- mobile-only //end  -->


			</div> <!-- flex grid //end -->
		</div> <!-- container //end -->
	</header>
	<nav class="relative shadow-sm" :class="{hidden: !state.openMenu}">
		<div class="container max-w-screen-xl mx-auto px-4">
			<!-- Bottom -->
			<div class="lg:flex flex-1 items-center py-1">
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> Category </a>
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> About </a>
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> Services </a>
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> Projects </a>
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> Offers </a>
				<a class="px-3 py-2 rounded-md hover:bg-gray-100" href="#"> Others </a>
			</div>
			<!-- Bottom //end -->
		</div> <!-- container //end -->
	</nav>
</template>
