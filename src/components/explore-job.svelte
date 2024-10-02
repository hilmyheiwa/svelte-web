<script>
    import image from "../assets/images/company/facebook-logo.png";
    import image2 from "../assets/images/company/google-logo.png";
    import image3 from "../assets/images/company/android.png";
    import image4 from "../assets/images/company/lenovo-logo.png";
    import image5 from "../assets/images/company/spotify.png";
    import image6 from "../assets/images/company/linkedin.png";
    import { navigate } from "svelte-routing";

    const JobData = [
        {
            id: 1,
            image: image,
            name: "Facebook",
            time: "2 days ago",
            type: "Full Time",
            title: "Web Designer / Developer",
            city: "Australia",
        },
        {
            id: 2,
            image: image2,
            name: "Google",
            time: "2 days ago",
            type: "Part Time",
            title: "Marketing Director",
            city: "Australia",
        },
        {
            id: 3,
            image: image3,
            name: "Android",
            time: "2 days ago",
            type: "Remote",
            title: "Application Developer",
            city: "Australia",
        },
        {
            id: 4,
            image: image4,
            name: "Lenovo",
            time: "2 days ago",
            type: "WFH",
            title: "Senior Product Designer",
            city: "Australia",
        },
        {
            id: 5,
            image: image5,
            name: "Spotify",
            time: "2 days ago",
            type: "Full Time",
            title: "C++ Developer",
            city: "Australia",
        },
        {
            id: 6,
            image: image6,
            name: "Linkedin",
            time: "2 days ago",
            type: "Remote",
            title: "Php Developer",
            city: "Australia",
        },
    ];
</script>

<main>
    <div class="row align-items-end mb-4 pb-2">
        <div class="col-lg-6 col-md-9">
            <div class="section-title text-md-start text-center">
                <h4 class="title mb-3">Explore Jobs</h4>
                <p class="text-muted para-desc mb-0">
                    Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+
                    companies worldwide.
                </p>
            </div>
        </div>
        <!--end col-->

        <div class="col-lg-6 col-md-3 d-none d-md-block">
            <div class="text-md-end">
                <a
                    href="/job-grid-one"
                    class="btn btn-link primary text-muted"
                    on:click={() => navigate("/job-grid-one")}
                    >See More Jobs <i class="mdi mdi-arrow-right"></i></a
                >
            </div>
        </div>
        <!--end col-->
    </div>
    <!--end row-->

    <div class="row g-4 mt-0">
        {#each JobData as item}
            <div class="col-lg-4 col-md-6 col-12">
                <div class="job-post rounded shadow p-4">
                    <div
                        class="d-flex align-items-center justify-content-between"
                    >
                        <div class="d-flex align-items-center">
                            <img
                                src={item.image}
                                class="avatar avatar-small rounded shadow p-3 bg-white"
                                alt=""
                            />

                            <div class="ms-3">
                                <a
                                    href={`/employer-profile/${item.id}`}
                                    class="h5 company text-dark"
                                >
                                    {item.name}
                                </a>
                                <span
                                    class="text-muted d-flex align-items-center small mt-2"
                                >
                                    <i
                                        data-feather="clock"
                                        class="fea icon-sm me-1"
                                    ></i>
                                    {item.time}
                                </span>
                            </div>
                        </div>

                        <span class="badge bg-soft-primary">{item.type}</span>
                    </div>

                    <div class="mt-4">
                        <a
                            href={`/job-detail-one/${item.id}`}
                            class="text-dark title h5"
                        >
                            {item.title}
                        </a>

                        <span class="text-muted d-flex align-items-center mt-2">
                            <i data-feather="map-pin" class="fea icon-sm me-1"
                            ></i>
                            {item.city}
                        </span>

                        <div class="progress-box mt-3">
                            <div class="progress mb-2">
                                <div
                                    class="progress-bar position-relative bg-primary"
                                    style={`width: 50%;`}
                                ></div>
                            </div>

                            <span class="text-dark">
                                20 applied of <span class="text-muted"
                                    >40 vacancy</span
                                >
                            </span>
                        </div>
                    </div>
                </div>
                <!--end job post-->
            </div>
            <!--end col-->
        {/each}
    </div>
    <!--end row-->
</main>

<style lang="scss" scoped></style>
