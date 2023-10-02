<script setup lang="ts">
import { ref } from "vue";
import MapMarkerOutlineIcon from "vue-material-design-icons/MapMarkerOutline.vue";
import MenuDownIcon from "vue-material-design-icons/MenuDown.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue";
import CartMinusIcon from "vue-material-design-icons/CartMinus.vue";
import { Link } from "@inertiajs/vue3";

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div class="min-w-[1150px] bg-gray-100 h-full">
        <header
            class="flex items-center w-full bg-gray-900 h-[60px] py-2 fixed z-50 min-w-[1150px]"
        >
            <div class="flex">
                <Link
                    href="/"
                    class="uppercase h-[50px] px-2 cursor-pointer text-white pt-3 border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    amazon
                </Link>
            </div>

            <div
                class="uppercase h-[50px] p-2 cursor-pointer text-white border border-gray-900 rounded-sm hover:border hover:border-gray-100"
            >
                <div class="flex items-center justify-center">
                    <MapMarkerOutlineIcon
                        class="pt-2 -ml-1"
                        fillColor="#f5f5f5"
                    />

                    <div>
                        <div class="text-[13px] text-gray-300 font-extrabold">
                            <div>Delivery to:</div>
                        </div>
                        <div
                            class="text-[15px] text-white -mt-1.5 font-extrabold"
                        >
                            <div>Colombia, Medellin</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex grow items-center px-1 h-[45px]">
                <div
                    class="flex items-center justify-center bg-gray-100 text-[11px] border-r border-r-gray-300 font-extrabold text-gray-600 w-[60px] h-[40px] rounded-l-md cursor-pointer"
                >
                    <div class="pt-[3px]">All</div>
                    <MenuDownIcon
                        fillColor="#5E5E5E"
                        :size="20"
                        class="-mr-2"
                    />
                </div>
                <input
                    type="text"
                    class="block w-full border-none border-transparent focus:border-transparent focus:ring-0"
                />
                <div
                    class="cursor-pointer bg-orange-300 py-[5px] px-2 rounded-r-md"
                >
                    <MagnifyIcon :size="30" />
                </div>
            </div>

            <div class="flex">
                <div
                    class="uppercase h-[50px] p-2 cursor-pointer border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    <div class="flex items-center justify-center mt-2.5 px-1">
                        <img src="https://via.placeholder.com/35x20" alt="" />
                        <div
                            class="text-[15px] text-white -mt-2 -mr-0.5 font-extrabold"
                        >
                            EN
                        </div>
                        <MenuDownIcon
                            fillColor="#c2c2c2"
                            :size="20"
                            class="-mr-4 -mt-1.5 pr-1"
                        />
                    </div>
                </div>

                <div
                    class="uppercase h-[50px] px-2 cursor-pointer border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    <div class="flex items-center">
                        <div class="flex items-center justify-center">
                            <div class="flex flex-col mt-2">
                                <div
                                    class="text-white font-extrabold text-[11px]"
                                >
                                    Hello, <span>sign in</span>
                                </div>
                                <div
                                    class="flex text-[15px] text-white -mt-1.5 font-extrabold"
                                >
                                    Account & List
                                    <MenuDownIcon
                                        fillColor="#c2c2c2"
                                        :size="20"
                                        class="-mr-4 self-end -mt-1 pr-1"
                                    />
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div
                    class="uppercase h-[50px] px-2 cursor-pointer border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    <div class="flex items-center">
                        <div class="flex items-center justify-center">
                            <div class="flex flex-col mt-2">
                                <div
                                    class="text-white font-extrabold text-[11px]"
                                >
                                    Returns
                                </div>
                                <div
                                    class="flex text-[15px] text-white -mt-1.5 font-extrabold"
                                >
                                    & Orders
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div
                    class="relative uppercase h-[50px] px-2 cursor-pointer border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    <span
                        class="absolute text-center right-[21px] w-[14px] -top-2 rounded-full text-[20px]"
                    >
                        <div
                            class="text-orange-400 font-extrabold bg-gray-900 h-[16px]"
                        >
                            0
                        </div>
                    </span>
                    <div class="flex items-center">
                        <CartMinusIcon
                            fillColor="#FCFCFC"
                            :size="40"
                            class="-mt-0.5"
                        />
                    </div>
                </div>
            </div>
        </header>

        <main>
            <div class="pt-[98px]"></div>
            <slot />
        </main>

        <div class="w-full bg-white mt-10">
            <div class="max-w-[1500px] mx-auto">
                <div class="text-[23px] pt-4 font-extrabold">
                    Recommended based on your shopping trends
                </div>
                <div class="flex justify-center items-stretch">
                    <div class="p-4 text-center mx-auto">
                        <div class="w-[158px] h-[150px] overflow-hidden">
                            <img
                                src="https://via.placeholder.com/158x150"
                                alt=""
                            />
                        </div>
                        <div
                            class="w-[160px] text-[12px] py-2 text-teal-600 font-extrabold hover:text-red-600 cursor-pointer"
                        >
                            This is a test title
                        </div>
                        <div class="flex justify-start">
                            <div
                                class="text-xs font-extrabold text-red-600 w-full text-left"
                            >
                                $99.99
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <footer class="bg-[#232F3E]">
            <div
                class="bg-[#37475A] hover:bg-gray-600 w-full p-3.5 cursor-pointer text-white font-extrabold text-center"
            >
                Back to top
            </div>
            <div
                class="flex items-stretch justify-between max-w-[1000px] mx-auto text-white p-10"
            >
                <ul>
                    <li class="font-extrabold text-lg">Get to Know Us</li>
                    <li class="hover:underline cursor-pointer">Carrers</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">
                        Investor Relations
                    </li>
                </ul>

                <ul>
                    <li class="font-extrabold text-lg">Get to Know Us</li>
                    <li class="hover:underline cursor-pointer">Carrers</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">
                        Investor Relations
                    </li>
                </ul>

                <ul>
                    <li class="font-extrabold text-lg">Get to Know Us</li>
                    <li class="hover:underline cursor-pointer">Carrers</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">About</li>
                    <li class="hover:underline cursor-pointer">
                        Investor Relations
                    </li>
                </ul>
            </div>
        </footer>
    </div>
</template>
