<script setup>
import Dropdown from '../Minimal/Dropdown.vue';
import ThemeController from '../Minimal/ThemeController.vue';
</script>

<template>
    <header>
        <nav class="bg-base-200 py-5 rounded-b-3xl">
            <div class="flex justify-between items-center">
                <a class="flex items-center pl-10 ">
                    <img src="https://flowbite.com/docs/images/logo.svg" class="mr-3 h-6 sm:h-9" alt="Flowbite Logo" />
                    <span class="self-center text-xl font-semibold whitespace-nowrap text-base-content">Flowbite</span>
                </a>
                <div class="join max-lg:hidden">
                    <Dropdown header-message="Hello" additional-header-style="btn-ghost join-item">
                        <template #HeaderIcon>
                            <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                                class="size-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                            </svg>
                        </template>
                        <template #Items>
                            <li><a>Item 1</a></li>
                            <li><a>Item 2</a></li>
                        </template>
                    </Dropdown>
                    <Dropdown header-message="Secondary Pages" additional-header-style="btn-ghost join-item">
                        <template #HeaderIcon>
                            <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                                class="size-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                            </svg>
                        </template>
                        <template #Items>
                            <li><a>Item 1</a></li>
                            <li><a>Item 2</a></li>
                        </template>
                    </Dropdown>
                    <Dropdown header-message="Account Pages" additional-header-style="btn-ghost join-item">
                        <template #HeaderIcon>
                            <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                                class="size-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
                            </svg>
                        </template>
                        <template #Items>
                            <li><a>Item 1</a></li>
                            <li><a>Item 2</a></li>
                        </template>
                    </Dropdown>
                </div>
                <div class="join pr-5">
                    <ThemeController></ThemeController>
                    <div class="max-lg:hidden">
                        <button class="btn btn-ghost join-item">Log in</button>
                        <button class="btn btn-ghost join-item">Get Started</button>
                    </div>
                    <div class="lg:hidden">
                        <Dropdown additional-dropdown-style="dropdown-bottom dropdown-end"
                            additional-header-style="btn-ghost join-item">
                            <template #HeaderIcon>
                                <svg fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                                    class="size-6">
                                    <path stroke-linecap="round" stroke-linejoin="round"
                                        d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                                </svg>
                            </template>
                            <template #Items>
                                <Dropdown header-message="Hello"
                                    additional-header-style="btn-ghost btn-block hover:bg-base-300 justify-between"
                                    >
                                    <template #HeaderIcon>
                                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                            stroke-width="1.5" stroke="currentColor" class="size-4">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M15.75 19.5 8.25 12l7.5-7.5" />
                                        </svg>

                                    </template>
                                    <template #Items>
                                        <li><a>Item 1 e</a></li>
                                        <li><a>Item 2 </a></li>
                                    </template>
                                </Dropdown>
                                <Dropdown header-message="Secondary Pages"
                                    additional-header-style="btn-ghost btn-block hover:bg-base-300 justify-between">
                                    <template #HeaderIcon>
                                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                            stroke-width="1.5" stroke="currentColor" class="size-4">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M15.75 19.5 8.25 12l7.5-7.5" />
                                        </svg>

                                    </template>
                                    <template #Items>
                                        <li><a>Item 1</a></li>
                                        <li><a>Item 2</a></li>
                                    </template>
                                </Dropdown>
                                <Dropdown header-message="Account Pages"
                                    additional-header-style="w-full bg-transparent border-none  hover:bg-base-300 justify-between">
                                    <template #HeaderIcon>
                                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                            stroke-width="1.5" stroke="currentColor" class="size-4">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M15.75 19.5 8.25 12l7.5-7.5" />
                                        </svg>

                                    </template>
                                    <template #Items>
                                        <li><a>Item 1</a></li>
                                        <li><a>Item 2</a></li>
                                    </template>
                                </Dropdown>
                                <li><a>Log In</a></li>
                                <li><a>Get Started</a></li>
                            </template>
                        </Dropdown>
                    </div>

                </div>
            </div>
        </nav>
    </header>
</template>