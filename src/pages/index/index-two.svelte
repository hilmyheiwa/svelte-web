<script>
    import Navbar from "../../components/navbar.svelte";
    import image from '../../assets/images/hero/bg.jpg';
    import Selectjob from '../../components/select-job.svelte';
    import Shape from '../../components/shape.svelte';
    import Services from '../../components/trending-services.svelte';
    import About from '../../components/about-index.svelte';
    import Joblisting from '../../components/popular-job-listing.svelte';
    import Companies from '../../components/companies-job.svelte';
    import Blogs from '../../components/blog.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte'
</script>

<main>
    <Navbar logoLight={true} navLight={'nav-light'} />

    <section class="bg-half-260 d-table w-100" style={ `background-image: url(${image})`} >
        <div class="bg-overlay bg-primary-gradient-overlay"></div>
        <div class="container">
            <div class="row mt-5 justify-content-center">
                <div class="col-lg-10">
                    <div class="title-heading text-center">
                        <h1 class="heading text-white fw-bold">Find & Hire Experts <br> for any Job</h1>
                        <p class="para-desc text-white-50 mx-auto mb-0">Find Jobs, Employment & Career Opportunities.
                            Some of the companies we've helped recruit excellent applicants over the years.</p>

                        <Selectjob selectjob={'p-2 mt-4'} />

                        <div class="mt-2">
                            <span class="text-white-50"><span class="text-white">Popular Searches :</span> Designer,
                                Developer, Web, IOS, PHP Senior Engineer</span>
                        </div>
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div><!--end container-->
    </section><!--end section-->
    <Shape />

    <section class="section">
        <Services />
        <div class="container mt-100 mt-60">
            <About />
        </div>
        <div class="container mt-100 mt-60">
            <Joblisting />
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
