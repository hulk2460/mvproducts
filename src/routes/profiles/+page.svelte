<script lang="ts">
  import Table from "$lib/Table.svelte";

  /** @type {import('./$types').PageData} */
  export let data;
  console.log("hello", data.names);

  /** @type {import('./$types').ActionData} */
  export let form;
</script>


<section class="bg-gray-50 dark:bg-gray-900">
  <div class="flex flex-col items-center justify-center px-3 py-3 mx-auto md:h-screen lg:py-0">
      <a href="#" class="flex items-center mb-6 text-3xl  font-semibold text-gray-900 dark:text-white">
          
          User Login    
      </a>
      <div class="w-full bg-amber-200 rounded-lg shadow dark:border md:mt-0 sm:max-w-md xl:p-0 dark:bg-gray-800 dark:border-gray-700">
          <div class="p-6 space-y-4 md:space-y-6 sm:p-8">
              <h1 class="text-xl font-bold leading-tight tracking-tight text-gray-900 md:text-2xl dark:text-white">
                  Welcome Back
              </h1>
              <form class="space-y-4 md:space-y-6" action="#">
                  <div>
                      <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Enter your email</label>
                      <input type="email" name="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="name@company.com" required="">
                  </div>
                  <div>
                      <label for="password" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Enter your password</label>
                      <input type="password" name="password" id="password" placeholder="••••••••" class="bg-gray-50 border border-gray-300 text-gray-900 rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" required="">
                  </div>
                  
                  <button type="submit" class="w-full text-black bg-lime-400 hover:bg-primary-700 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800">Login</button>
                  <p class="text-sm font-light text-gray-500 dark:text-gray-400">
                      Don’t have an account? <a href="register" class="font-medium text-primary-600 hover:underline dark:text-primary-500">Register</a>
                  </p>
              </form>
          </div>
      </div>
  </div>
</section>
  {#if form?.success}
    <!-- this message is ephemeral; it exists because the page was rendered in
		   response to a form submission. it will vanish if the user reloads -->
    <p class="pt-2">Login successful !!! 🥳  </p>
  {/if}

<div class="h-32"></div>
