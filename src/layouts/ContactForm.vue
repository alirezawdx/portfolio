<template>
  <form class="flex justify-center items-cetner flex-col gap-5 w-full md:w-1/3 text-left px-5">
    <div class="flex-grow">
      <label for="fullName" class="font-medium dark:text-white">Full Name</label>
      <input
        required
        type="text"
        name="fullName"
        id="fullNameInput"
        class="block border py-4 px-5 rounded-lg mt-3 w-full dark:text-[#E1E1E1]"
        placeholder="John Doe"
      />
    </div>
    <div class="flex-grow">
      <label for="email" class="font-medium dark:text-white">Email</label>
      <input
        required
        type="email"
        name="email"
        id="emailInput"
        class="block border py-4 px-5 rounded-lg mt-3 w-full dark:text-[#E1E1E1]"
        placeholder="john@doe.com"
      />
    </div>
    <div class="flex-grow">
      <label for="service" class="font-medium dark:text-white">Service</label>
      <select
        required
        name="service"
        id="serviceInput"
        class="block border py-4 px-5 rounded-lg mt-3 w-full dark:text-[#E1E1E1]"
        placeholder="John Doe"
      >
        <option disabled selected>Select a service</option>
        <option value="frontend">Front-end Development</option>
        <option value="backend">Back-end Development</option>
      </select>
    </div>
    <div class="flex-grow">
      <label for="text" class="font-medium dark:text-white">Message</label>
      <textarea
        required
        type="text"
        name="text"
        id="textInput"
        class="block border py-4 px-5 rounded-lg mt-3 w-full dark:text-[#E1E1E1]"
        placeholder="Message here..."
        rows="5"
      ></textarea>
    </div>
    <SingleButton
      href="/none"
      class="py-4 text-center bg-[#484E53] text-white dark:bg-white dark:bg-white dark:text-black dark:border-white"
      >Get in touch</SingleButton
    >
  </form>
</template>
