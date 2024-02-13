<script lang="ts">
    import NavItem from "./NavItem.svelte";
    import Logo from "$lib/assets/Company_Logo.svg";
    import { isScrollBarAtTopOfPage } from "$lib/scrolling";
    import { onMount } from "svelte";

    const navItems = {
        about: {
            name: "About",
            href: "/about",
        },
        services: {
            name: "Services",
            href: "/services",
        },
        contact: {
            name: "Contact",
            href: "/contact",
        },
    };

    const handlePagePosition = (nav: HTMLElement) => {
        if (isScrollBarAtTopOfPage()) {
            nav.classList.remove("shadow-md");
            nav.classList.add("bg-base");
            nav.classList.remove("bg-crust");
        } else if (nav.classList.contains("bg-base")) {
            nav.classList.add("shadow-md");
            nav.classList.add("bg-crust");
            nav.classList.remove("bg-base");
        }
    };

    onMount(() => {
        const nav = document.getElementById("nav");

        if (!nav) {
            return;
        }

        window.addEventListener("scroll", () => {
            handlePagePosition(nav);
        });

        handlePagePosition(nav);
    });
</script>

<nav
    id="nav"
    class="fixed bg-base top-0 left-0 z-10 w-full flex flex-row justify-center lg:justify-between items-center py-4 px-8 transition-all"
>
    <div id="nav-logo">
        <a href="/"><img src={Logo} alt="logo" class="w-10 text-black" /></a>
    </div>

    <div id="nav-buttons" class="max-md:hidden">
        <ul class="flex flex-row justify-center items-center gap-6">
            {#each Object.values(navItems) as item}
                <li>
                    <NavItem {...item} />
                </li>
            {/each}
        </ul>
    </div>

    <div id="nav-menu" class="absolute left-0 top-2 lg:hidden"></div>
</nav>
