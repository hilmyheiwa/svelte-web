<script>
    import Navbar from "../../components/navbar.svelte";
    import image from '../../assets/images/hero/bg.jpg';
    import logo from '../../assets/images/company/lenovo-logo.png'
    import { Link } from "svelte-routing";
    import Shape from "../../components/shape.svelte";
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from "../../components/back-to-top.svelte";
    import Applyjob from '../../components/job-apply.svelte'

</script>

<main>
    <Navbar logoLight={true} navLight={'nav-light'} />
    <section class="bg-half-170 d-table w-100"
    style={`background-image: url(${image}); background-position: top`}>
    <div class="bg-overlay bg-gradient-overlay"></div>
    <div class="container">
        <div class="row mt-5 justify-content-center">
            <div class="col-12">
                <div class="title-heading text-center">
                    <img src={logo}
                        class="avatar avatar-small rounded-pill p-2 bg-white" alt="">
                    <h5 class="heading fw-semibold mb-0 sub-heading text-white title-dark mt-3">Back-End Developer
                    </h5>
                </div>
            </div><!--end col-->
        </div><!--end row-->

        <div class="position-middle-bottom">
            <nav aria-label="breadcrumb" class="d-block">
                <ul class="breadcrumb breadcrumb-muted mb-0 p-0">
                    <li class="breadcrumb-item"><Link to="/">Jobnova</Link></li>
                    <li class="breadcrumb-item"><Link to="/job-grid-one">Job</Link></li>
                    <li class="breadcrumb-item active" aria-current="page">Job Apply</li>
                </ul>
            </nav>
        </div>
    </div><!--end container-->
</section><!--end section-->
 <Shape />

 <section class="section bg-light">
    <Applyjob />
</section>
<Footers explore={true} footerbar={'footer-bar'} />
<Backtotop />

</main>

<style>

</style>