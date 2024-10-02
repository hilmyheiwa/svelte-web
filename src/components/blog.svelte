<script>
    import image from "../assets/images/blog/01.jpg";
    import image2 from "../assets/images/blog/02.jpg";
    import image3 from "../assets/images/blog/03.jpg";

    const datas = [
        {
            id: 1,
            image: image,
            type: "Arts",
            title: "11 Tips to Help You Get New Clients Through Cold Calling",
            company: "Google",
        },
        {
            id: 2,
            image: image2,
            type: "Illustration",
            title: "DigitalOcean launches first Canadian data centre in Toronto",
            company: "Facebook",
        },
        {
            id: 3,
            image: image3,
            type: "Music",
            title: "Using Banner Stands To Increase Trade Show Traffic",
            company: "Linkedin",
        },
    ];
</script>

<main>
    <div class="row justify-content-center">
        <div class="col">
            <div class="section-title text-center mb-4 pb-2">
                <h4 class="title mb-3">Latest Blog or News</h4>
                <p class="text-muted para-desc mb-0 mx-auto">
                    Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+
                    companies worldwide.
                </p>
            </div>
        </div>
        <!--end col-->
    </div>
    <!--end row-->

    <div class="row g-4 mt-0">
        {#each datas as item}
            <div class="col-lg-4 col-md-6">
                <div
                    class="card blog blog-primary shadow rounded overflow-hidden border-0"
                >
                    <div
                        class="card-img blog-image position-relative overflow-hidden rounded-0"
                    >
                        <div class="position-relative overflow-hidden">
                            <img src={item.image} class="img-fluid" alt="" />
                            <div class="card-overlay"></div>
                        </div>
                    </div>

                    <div class="card-body blog-content position-relative p-0">
                        <div class="blog-tag px-4">
                            <a
                                href="#type"
                                class="badge bg-primary rounded-pill"
                                >{item.type}</a
                            >
                        </div>
                        <div class="p-4">
                            <ul class="list-unstyled text-muted small mb-2">
                                <li
                                    class="d-inline-flex align-items-center me-2"
                                >
                                    <i
                                        data-feather="calendar"
                                        class="fea icon-ex-sm me-1 text-dark"
                                    ></i>31st October 2023
                                </li>
                                <li class="d-inline-flex align-items-center">
                                    <i
                                        data-feather="clock"
                                        class="fea icon-ex-sm me-1 text-dark"
                                    ></i>5 min read
                                </li>
                            </ul>

                            <a
                                href={`/blog-detail/${item.id}`}
                                class="title fw-semibold fs-5 text-dark"
                                >{item.title}</a
                            >

                            <ul
                                class="list-unstyled d-flex justify-content-between align-items-center text-muted mb-0 mt-3"
                            >
                                <li class="list-inline-item me-2">
                                    <a
                                        href="#read"
                                        class="btn btn-link primary text-dark"
                                        >Read Now
                                        <i class="mdi mdi-arrow-right"></i></a
                                    >
                                </li>
                                <li class="list-inline-item">
                                    <span class="text-dark">By</span>
                                    <a
                                        href="company"
                                        class="text-muted link-title"
                                        >{item.company}</a
                                    >
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
            <!--end col-->
        {/each}
    </div>
    <!--end row-->
</main>

<style lang="scss" scoped></style>
