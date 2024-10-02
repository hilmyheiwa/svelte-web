<script>
    import { Link } from 'svelte-routing';
    import Navbar from '../../components/navbar.svelte';
    import image from '../../assets/images/hero/bg.jpg';
    import Shape from '../../components/shape.svelte';
    import Services from '../../components/services-job.svelte';
    import About from '../../components/about-index.svelte';
    import Jobopening from '../../components/job-opening.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte'
    
    </script>

<main>
    <Navbar navLight={'nav-light'} logoLight={true} />

    <section class="bg-half-170 d-table w-100"
        style={ `background-image: url(${image}); background-position: top` }>
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row mt-5 justify-content-center">
                <div class="col-12">
                    <div class="title-heading text-center">
                        <h5 class="heading fw-semibold mb-0 sub-heading text-white title-dark">Job Opening</h5>
                    </div>
                </div><!--end col-->
            </div><!--end row-->

            <div class="position-middle-bottom">
                <nav aria-label="breadcrumb" class="d-block">
                    <ul class="breadcrumb breadcrumb-muted mb-0 p-0">
                        <li class="breadcrumb-item"><Link to="/">Jobnova</Link></li>
                        <li class="breadcrumb-item active" aria-current="page">Career</li>
                    </ul>
                </nav>
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <Shape />

    <section class="section">
        <div class="container">
            <Services information={true} />
        </div>
        <div class="container mt-100 mt-60">
            <About />
        </div>
        <div class="container mt-100 mt-60">
            <Jobopening />
        </div>
    </section>
    <Footers explore={true} footerbar={'footer-bar'} />
    <Backtotop />
</main>

<style lang="scss" scoped></style>