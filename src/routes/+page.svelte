<script lang="ts">
    import Icon from "@iconify/svelte";

    const scrollToServiceOverview = () => {
        const serviceOverview = document.getElementById("service-overview");
        serviceOverview?.scrollIntoView({
            behavior: "smooth",
            block: "start",
            inline: "nearest",
        });
    };
</script>

<div
    id="main-hero"
    class="bg-base flex flex-row justify-center items-center gap-16 lg:p-8 text-center h-screen lg:h-[75vh]"
>
    <div class="[&>*]:m-3">
        <h1 class="text-6xl font-bold text-green">Cash Consulting, LLC</h1>
        <button
            class="bg-green/80 hover:bg-green transition-colors rounded text-white p-3"
        >
            Schedule a service
        </button>
    </div>

    <div class="absolute bottom-3 left-0 right-0 visible lg:hidden bounce p-0">
        <button on:click={scrollToServiceOverview}>
            <Icon icon="mdi:chevron-down" width="100" class="text-green" />
        </button>
    </div>
</div>

<div
    id="service-overview"
    class="w-full flex flex-col justify-center items-center px-8 pb-5"
>
    <div class="bg-mantle flex flex-col max-md:p-3 lg:p-8 rounded-lg shadow-lg">
        <h1 class="text-3xl font-bold mb-8">
            We offer a lot, but we take little...
        </h1>
        <div class="grid grid-rows-3">
            <div class="flex flex-row justify-center items-center [&>*]:m-3">
                <Icon
                    icon="mdi:home"
                    width="100"
                    class="text-green max-md:hidden"
                />
                <p class="text-md font-bold">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique,
                    similipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique
                    similipsum
                </p>
            </div>
            <div class="flex flex-row justify-center items-center [&>*]:m-3">
                <p class="text-md font-bold">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique,
                    similipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique
                    similipsum
                </p>
                <Icon
                    icon="mdi:clipboard"
                    width="100"
                    class="text-green max-md:hidden"
                />
            </div>
            <div class="flex flex-row justify-center items-center [&>*]:m-3">
                <Icon
                    icon="mdi:camera"
                    width="100"
                    class="text-green max-md:hidden"
                />
                <p class="text-md font-bold">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique,
                    similipsum dolor sit amet consectetur adipisicing elit.
                    Totam ullam sint doloremque nemo suscipit, similique
                    similipsum
                </p>
            </div>
        </div>
    </div>
</div>

<style lang="postcss">
    .bounce {
        animation: bounce 2s infinite;
    }

    @keyframes bounce {
        0%,
        100% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(-10px);
        }
    }
</style>
