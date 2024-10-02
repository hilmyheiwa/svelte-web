<script>
    import { onMount } from "svelte";
    import { tns } from "tiny-slider/src/tiny-slider";
    import feather from "feather-icons";

    const datas = [
        {
            icon: "airplay",
            name: "Business",
            nametwo: "Development",
            job: "74 Jobs",
        },
        {
            icon: "award",
            name: "Marketing &",
            nametwo: "Communication",
            job: "20 Jobs",
        },
        {
            icon: "at-sign",
            name: "Project",
            nametwo: "Management",
            job: "35 Jobs",
        },
        {
            icon: "codesandbox",
            name: "Customer",
            nametwo: "Service",
            job: "46 Jobs",
        },
        {
            icon: "chrome",
            name: "Software",
            nametwo: "Engineering",
            job: "60 Jobs",
        },
        {
            icon: "copy",
            name: "Human Resource",
            nametwo: "HR",
            job: "74 Jobs",
        },
        {
            icon: "cpu",
            name: "It &",
            nametwo: "Networking",
            job: "20 Jobs",
        },
    ];

    onMount(() => {
        tns({
            container: ".tiny-five-item",
            controls: true,
            mouseDrag: true,
            loop: true,
            rewind: true,
            autoplay: true,
            autoplayButtonOutput: false,
            autoplayTimeout: 3000,
            navPosition: "bottom",
            controlsText: [
                '<i class="mdi mdi-chevron-left "></i>',
                '<i class="mdi mdi-chevron-right"></i>',
            ],
            nav: false,
            speed: 400,
            gutter: 0,
            responsive: {
                1025: {
                    items: 5,
                },

                992: {
                    items: 4,
                },

                767: {
                    items: 3,
                },

                425: {
                    items: 1,
                },
            },
        });
        feather.replace();
    });
</script>

<main>
    <div class="row justify-content-center mb-4 pb-2">
        <div class="col-12">
            <div class="section-title text-center">
                <h4 class="title mb-3">Popular Categories</h4>
                <p class="text-muted para-desc mx-auto mb-0">
                    Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+
                    companies worldwide.
                </p>
            </div>
        </div>
        <!--end col-->
    </div>
    <!--end row-->

    <div class="row">
        <div class="col-12 mt-4">
            <div class="tiny-five-item">
                {#each datas as item}
                    <div class="tiny-slide">
                        <div
                            class="position-relative job-category text-center px-4 py-5 rounded shadow m-2"
                        >
                            <div
                                class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center"
                            >
                                {#if item.icon}
                                    <i
                                        class="fea icon-ex-md"
                                        data-feather={item.icon}
                                    ></i>
                                {/if}
                            </div>

                            <div class="mt-4">
                                <a href="#name" class="title h5 text-dark"
                                    >{item.name} <br /> {item.nametwo}</a
                                >
                                <p class="text-muted mb-0 mt-3">{item.job}</p>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</main>

<style>
</style>
