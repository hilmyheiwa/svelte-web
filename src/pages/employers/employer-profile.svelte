<script>
import { Link } from 'svelte-routing';
import Navbar from '../../components/navbar.svelte';
import imagebg from '../../assets/images/hero/bg4.jpg';
import Shape from '../../components/shape.svelte';
import Company from '../../components/employers/company-story.svelte';
import Related from '../../components/employers/related-companies.svelte';
import Footers from '../../components/footer/footer.svelte';
import Backtotop from '../../components/back-to-top.svelte';
import image4 from '../../assets/images/company/lenovo-logo.png'
</script>

<main>
    <Navbar navLight={'nav-light'} logoLight={true} />
    <section class="bg-half-170 d-table w-100"
        style={ `background-image: url(${imagebg}); background-position: top` }>
        <div class="bg-overlay bg-gradient-overlay-2"></div>
    </section><!--end section-->
    <Shape />

    <section class="section">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-12 mt-4">
                    <div class="features-absolute">
                        <div class="d-md-flex justify-content-between align-items-center bg-white shadow rounded p-4">
                            <div class="d-flex align-items-center">
                                <img src={image4} class="avatar avatar-md-md rounded shadow p-3 bg-white" alt="">

                                <div class="ms-3">
                                    <h5>Lenovo</h5>
                                    <span class="text-muted d-flex align-items-center"><i data-feather="map-pin"
                                            class="fea icon-sm me-1"></i>anberra, Australia</span>
                                </div>
                            </div>

                            <div class="mt-4 mt-md-0">
                                <Link to="#" class="btn btn-sm btn-primary me-1">Follow</Link>
                                <Link to="/job-grid-one" class="btn btn-sm btn-soft-primary">See
                                    Jobs</Link>
                            </div>
                        </div>
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div><!--end container-->

        <div class="container">
            <Company />
            <div class="container mt-100 mt-60">
                <Related />
            </div>
        </div>
    </section>
    <Footers explore={true} footerbar={'footer-bar'} />
    <Backtotop />
</main>

<style lang="scss" scoped></style>