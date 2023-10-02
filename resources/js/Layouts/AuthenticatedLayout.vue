<script setup lang="ts">
import { ref } from "vue";
import MapMarkerOutlineIcon from "vue-material-design-icons/MapMarkerOutline.vue";
import MenuDownIcon from "vue-material-design-icons/MenuDown.vue";
import MenuIcon from "vue-material-design-icons/Menu.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue";
import CartMinusIcon from "vue-material-design-icons/CartMinus.vue";
import AccountCircleIcon from "vue-material-design-icons/AccountCircle.vue";
import CloseIcon from "vue-material-design-icons/Close.vue";
import ChevronRightIcon from "vue-material-design-icons/ChevronRight.vue";

import { Link } from "@inertiajs/vue3";

const showMenu = ref(false);
const accountAndList = ref(false);

const handleAccoundAndList = (bool: boolean) => {
    setTimeout(() => {
        accountAndList.value = bool;
    }, 150);
};
</script>

<template>
    <div class="min-w-[1150px] bg-gray-100 h-full">
        <div
            v-if="accountAndList"
            class="top-0 z-20 fixed w-full h-full bg-black bg-opacity-70"
        ></div>
        <header
            class="flex items-center w-full bg-gray-900 h-[60px] py-2 fixed z-50 min-w-[1150px]"
        >
            <div class="flex">
                <Link
                    href="/"
                    class="uppercase h-[50px] px-2 cursor-pointer text-white pt-3 border border-gray-900 rounded-sm hover:border hover:border-gray-100"
                >
                    <img
                        src="/images/logo/AMAZON_LOGO.png"
                        width="100"
                        alt=""
                    />
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
                        <img
                            src="/images/flags/US.png"
                            class="mb-3 mr-1"
                            width="23"
                            alt=""
                        />
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
                    @mouseenter="handleAccoundAndList(true)"
                    @mouseleave="handleAccoundAndList(false)"
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
                        <div
                            v-if="accountAndList"
                            class="bg-white absolute z-50 top-[56px] -ml-[230px] w-[480px] rounded-sm px-6"
                        >
                            <div>
                                <div
                                    class="flex items-center justify-between py-2.5 border-b"
                                >
                                    <div class="text-sm p-2">
                                        Who's shopping? Select a profile.
                                    </div>
                                    <div
                                        class="flex items-center text-sm font-bold text-teal-600 hover:text-red-600 hover:underline"
                                    >
                                        Manage Profile
                                        <ChevronRightIcon
                                            :size="20"
                                            fillColor="#808080"
                                        />
                                    </div>
                                </div>

                                <div class="flex">
                                    <div class="w-1/2 border-r">
                                        <div class="pb-3">
                                            <div class="font-extrabold pt-3">
                                                Your list
                                            </div>
                                            <div
                                                class="text-sm hover:text-red-600 hover:underline pt-3"
                                            >
                                                Create a list
                                            </div>
                                        </div>
                                    </div>

                                    <div class="w-1/2 ml-5">
                                        <div class="pb-3">
                                            <div class="font-extrabold pt-3">
                                                Your Account
                                            </div>
                                            <div
                                                class="text-sm hover:text-red-600 hover:underline pt-3"
                                            >
                                                Account
                                            </div>
                                            <div
                                                class="text-sm hover:text-red-600 hover:underline pt-3"
                                            >
                                                Sign Out
                                            </div>
                                        </div>
                                    </div>
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

        <div
            class="flex justify-between items-center bg-[#232f3e] h-[38px] fixed z-40 min-w-[1150px] w-full mt-[60px]"
        >
            <div class="flex">
                <div
                    @click="showMenu = true"
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <MenuIcon
                            fillColor="#F5F5F5"
                            :size="26"
                            class="mr-0.5"
                        />
                        <div class="text-[14px] text-white font-extrabold">
                            All
                        </div>
                    </div>
                </div>

                <div
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <div class="text-[14px] text-white font-extrabold">
                            Today's Deals
                        </div>
                    </div>
                </div>

                <div
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <div class="text-[14px] text-white font-extrabold">
                            Gift cards
                        </div>
                    </div>
                </div>
                <div
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <div class="text-[14px] text-white font-extrabold">
                            Buy again
                        </div>
                    </div>
                </div>

                <div
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <div class="text-[14px] text-white font-extrabold">
                            Customer Service
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex">
                <div
                    class="flex h-[30px] border border-[#232f3e] rounded-sm hover:border hover:border-gray-100 cursor-pointer"
                >
                    <div class="flex justify-between items-center px-2">
                        <div class="text-[14px] text-white font-extrabold">
                            Holiday Fasion Deals
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <main class="max-w-[1500px] mx-auto">
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

    <div
        v-if="showMenu"
        :class="[
            showMenu ? 'animate__animated animate__fadeIn animate__faster' : '',
        ]"
        class="top-0 z-50 fixed w-full h-full bg-black bg-opacity-70"
    >
        <CloseIcon
            @click="showMenu = false"
            :size="30"
            fillColor="#DCDCDC"
            :class="[
                showMenu
                    ? 'animate__animated animate__fadeIn animate__faster'
                    : '',
            ]"
            class="ml-2.5 mt-3.5 left-80 cursor-pointer fixed z-50"
        />
        <div
            :class="[
                showMenu
                    ? 'animate__animated animate__slideInLeft animate__faster'
                    : '',
            ]"
            class="w-80 h-full bg-white"
        >
            <div
                class="bg-[#232f3e] font-extrabold text-[18px] flex items-center p-2 text-white pl-7"
            >
                <span>Hello, sign in</span>
            </div>

            <div
                class="font-extrabold capitalize text-[16px] pt-3 pb-1 pl-6 pr-3 text-black"
            >
                Shop by departament
            </div>

            <div class="hover:bg-gray-200 pl-6 pr-3">
                <div
                    class="py-2.5 text-[13px] text-black flex justify-between items-center hover:bg-gray-200 cursor-pointer"
                >
                    Computers
                    <ChevronRightIcon :size="20" fillColor="#808080" />
                </div>
            </div>
        </div>
    </div>
</template>
