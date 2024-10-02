<script>
    import Navbar from "../../components/navbar.svelte";
    import hero from "../../assets/images/hero1.png";
    import circle from "../../assets/images/company/circle-logo.png";
    import facebook from "../../assets/images/company/facebook-logo.png";
    import google from "../../assets/images/company/google-logo.png";
    import lenovo from "../../assets/images/company/lenovo-logo.png";
    import android from "../../assets/images/company/android.png";
    import linkedin from "../../assets/images/company/linkedin.png";
    import skype from "../../assets/images/company/skype.png";
    import snapchat from "../../assets/images/company/snapchat.png";
    import backgrdimg from "../../assets/images/bg2.png";
    import feather from "feather-icons";
    import Aboutus from "../../components/about-index.svelte";
    import Categories from "../../components/popular-categories.svelte";
    import Explorejob from "../../components/explore-job.svelte";
    import Services from "../../components/services-job.svelte";
    import Companies from "../../components/companies-job.svelte";
    import Blogs from '../../components/blog.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte'

    let datas = [
        {
            class: "position-absolute top-0 start-0 mt-lg-5 mt-4 ms-lg-5 ms-4",
            image: circle,
        },
        {
            class: "position-absolute top-0 start-50 translate-middle-x",
            image: facebook,
        },
        {
            class: "position-absolute top-0 end-0 mt-lg-5 mt-4 me-lg-5 me-4",
            image: google,
        },
        {
            class: "position-absolute top-50 start-0 translate-middle-y",
            image: lenovo,
        },
        {
            class: "position-absolute top-50 end-0 translate-middle-y",
            image: android,
        },
        {
            class: "position-absolute bottom-0 start-0 mb-lg-5 mb-4 ms-lg-5 ms-4",
            image: linkedin,
        },
        {
            class: "position-absolute bottom-0 start-50 translate-middle-x",
            image: skype,
        },
        {
            class: "position-absolute bottom-0 end-0 mb-lg-5 mb-4 me-lg-5 me-4",
            image: snapchat,
        },
    ];

    feather.replace();
</script>

<main>
    <Navbar navLight={'nav-light'} />

    <section
        class="bg-half-170 d-table w-100 bg-primary"
        style={`background-image: url(${backgrdimg})`}
    >
        <div class="container">
            <div class="row g-4 align-items-center">
                <div class="col-md-6">
                    <div class="title-heading">
                        <h1 class="heading text-white fw-bold">
                            Get hired <br /> by the popular <br /> candidates.
                        </h1>
                        <p class="para-desc text-white-50 mb-0">
                            Find Jobs, Employment & Career Opportunities. Some
                            of the companies we've helped recruit excellent
                            applicants over the years.
                        </p>

                        <div class="text-center subscribe-form mt-4">
                            <form style="max-width: 800px;">
                                <div class="mb-0">
                                    <div class="position-relative">
                                        <i
                                            data-feather="search"
                                            class="fea icon-20 position-absolute top-50 start-0 translate-middle-y ms-3"
                                        ></i>
                                        <input
                                            type="text"
                                            id="help"
                                            name="name"
                                            class="shadow rounded-pill bg-white ps-5"
                                            required
                                            placeholder="Search jobs & candidates ..."
                                        />
                                    </div>
                                    <button
                                        type="submit"
                                        class="btn btn-primary btn-pills"
                                        >Search</button
                                    >
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
                <!--end col-->

                <div class="col-md-6">
                    <div class="position-relative ms-lg-5">
                        <img src={hero} class="img-fluid p-5" alt="" />

                        <div class="spinner">
                            {#each datas as item}
                                <div class={item.class}>
                                    <img
                                        src={item.image}
                                        class="avatar avatar-md-sm rounded shadow p-2 bg-white"
                                        alt=""
                                    />
                                </div>
                            {/each}
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

    <section class="section">
        <div class="container">
            <Aboutus />
        </div>
        <div class="container mt-100 mt-60">
            <Categories />
        </div>
        <div class="container mt-100 mt-60">
            <Explorejob />
        </div>
        <div class="container mt-100 mt-60">
            <Services information={true} />
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
