<script>
	import AboutIndex from '../../components/about-index.svelte';
    import Navbar from "../../components/navbar.svelte";
    import image from "../../assets/images/hero/bg3.jpg";
    import image2 from "../../assets/images/hero.jpg";
    import Counter from '../../components/counter.svelte';
    import Joblisting from '../../components/job-listing.svelte';
    import Categories from '../../components/browser-categories.svelte';
    import Companies from '../../components/companies-job.svelte';
    import Blogs from '../../components/blog.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte'

    let toggle = true;
    const youtubeId = "yba7hPeTSjk";

    function handler() {
        toggle = !toggle;
    }
</script>

<main>

    <Navbar logoLight={true} navLight={'nav-light'} />

    <section
        class="bg-half-260 pb-lg-0 pb-md-4 bg-primary d-table w-100"
        style={`background-image : url(${image})`}
    >
        <div class="bg-overlay bg-black" style="opacity: 0.8;"></div>
        <div class="container">
            <div class="row g-4 position-relative z-1">
                <div class="col-lg-7 col-md-6 col-12 mt-lg-5">
                    <div class="title-heading">
                        <h1 class="heading text-white title-dark mb-4">
                            Find a new job and <br /> build career
                        </h1>
                        <p class="para-desc text-white-50">
                            Find Jobs, Employment & Career Opportunities. Some
                            of the companies we've helped recruit excellent
                            applicants over the years.
                        </p>

                        <div
                            class="d-md-flex justify-content-between align-items-center bg-white shadow rounded p-2 mt-4"
                        >
                            <form class="card-body text-start">
                                <div
                                    class="registration-form text-dark text-start"
                                >
                                    <div class="row g-lg-0">
                                        <div class="col-lg-9 col-md-8 col-12">
                                            <div class="mb-3 mb-sm-0">
                                                <label for="name"
                                                    class="form-label d-none fs-6"
                                                    >Search :</label
                                                >
                                                <div
                                                    class="filter-search-form position-relative filter-border"
                                                >
                                                    <i
                                                        data-feather="search"
                                                        class="fea icon-20 icons"
                                                    ></i>
                                                    <input
                                                        name="name"
                                                        type="text"
                                                        id="job-keyword"
                                                        class="form-control filter-input-box bg-light border-0"
                                                        placeholder="Search your keaywords"
                                                    />
                                                </div>
                                            </div>
                                        </div>
                                        <!--end col-->

                                        <div class="col-lg-3 col-md-4 col-12">
                                            <input
                                                type="submit"
                                                id="search"
                                                name="search"
                                                style="height: 60px;"
                                                class="btn btn-primary searchbtn w-100"
                                                value="Search"
                                            />
                                        </div>
                                        <!--end col-->
                                    </div>
                                    <!--end row-->
                                </div>
                            </form>
                            <!--end form-->
                        </div>
                        <div class="mt-2">
                            <span class="text-white-50"
                                ><span class="text-white"
                                    >Popular Searches :</span
                                > Designer, Developer, Web, IOS, PHP Senior Engineer</span
                            >
                        </div>
                    </div>
                </div>
                <!--end col-->

                <div class="col-lg-5 col-md-6 col-12">
                    <div class="bg-white rounded shadow p-2 position-relative">
                        <img src={image2} class="img-fluid rounded" alt="" />

                        <div
                            class="position-absolute top-50 start-50 translate-middle"
                        >
                            <a
                                href="#youtube"
                                on:click|preventDefault={handler}
                                data-type="youtube"
                                data-id="yba7hPeTSjk"
                                class="avatar avatar-md-md rounded-pill shadow card d-flex justify-content-center align-items-center lightbox"
                            >
                                <i class="mdi mdi-play mdi-24px text-primary"
                                ></i>
                            </a>
                        </div>
                    </div>
                </div>
                <!--end col-->
            </div>
            <!--end row-->
        </div>
        <!--end container-->
    </section>
    <!--end section-->

    <div class="position-relative">
        <div class="shape overflow-hidden text-white">
            <svg
                viewBox="0 0 2880 250"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                    d="M720 125L2160 0H2880V250H0V125H720Z"
                    fill="currentColor"
                ></path>
            </svg>
        </div>
    </div>

    {#if !toggle}
        <div
            class="modal-video"
            tabindex="-1"
            role="dialog"
            aria-modal="true"
            aria-label="You just opened the modal video"
        >
            <div class="modal-video-body">
                <div class="modal-video-inner">
                    <div class="modal-video-movie-wrap">
                        <iframe
                            title="YouTube video player"
                            width="460"
                            height="230"
                            src={`https://www.youtube.com/embed/${youtubeId}?feature=oembed`}
                            frameborder="0"
                            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                            tabindex="-1"
                        ></iframe>
                        <a href="#video" on:click|preventDefault={handler}
                            ><i
                                class="mdi mdi-close m-3 h4 position-class title-icon"
                            ></i></a
                        >
                    </div>
                </div>
            </div>
        </div>
    {/if}

    <section class="section">
        <Counter />
        <div class="container mt-100 mt-60">
            <Joblisting />
        </div>
        <div class="container mt-100 mt-60">
            <AboutIndex />
        </div>
        <div class="container mt-100 mt-60">
            <Categories />
        </div>
        <div class="container mt-100 mt-60">
            <Companies />
        </div>
        <div class="container mt-100 mt-60">
            <Blogs />
        </div>
    </section>
    <Footers />
    <Backtotop />
</main>

<style>
</style>
