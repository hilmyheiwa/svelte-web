<script>
    import Navbar from "../../../components/navbar.svelte";
    import image from "../../../assets/images/hero/bg.jpg";
    import Shape from "../../../components/shape.svelte";
    import Selectjob from "../../../components/select-job.svelte";
    import Gridone from "../../../components/job-grid/grid-one.svelte";
    import Pagination from "../../../components/pagination.svelte";
    import Services from "../../../components/services-job.svelte";
    import Footers from '../../../components/footer/footer.svelte';
    import Backtotop from '../../../components/back-to-top.svelte'
</script>

<main>
    <Navbar logoLight={true} navLight={'nav-light'} />

    <section
        class="bg-half-170 d-table w-100"
        style={`background-image : url(${image}); background-position: top`}
    >
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row mt-5 justify-content-center">
                <div class="col-12">
                    <div class="title-heading text-center">
                        <h5
                            class="heading fw-semibold mb-0 sub-heading text-white title-dark"
                        >
                            Job Vacancies
                        </h5>
                    </div>
                </div>
                <!--end col-->
            </div>
            <!--end row-->
        </div>
        <!--end container-->
    </section>
    <!--end section-->
    <Shape />

    <section class="section">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-12 mt-4">
                    <div class="features-absolute">
                        <Selectjob selectjob={"p-4"} />
                    </div>
                </div>
                <!--end col-->
            </div>
            <!--end row-->
        </div>
        <!--end container-->

        <div class="container mt-60">
            <Gridone />
            <Pagination />
        </div>
        <div class="container mt-100 mt-60">
            <Services information={true} />
        </div>
    </section>

    <Footers explore={true} footerbar={"footer-bar"} />
    <Backtotop />
</main>

<style>
</style>
