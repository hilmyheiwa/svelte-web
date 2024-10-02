<script>
    import { Link } from 'svelte-routing';
    import Navbar from '../../components/navbar.svelte';
    import imagebg from '../../assets/images/hero/bg.jpg';
    import Shape from '../../components/shape.svelte';
    import Detail from '../../components/blogs/blog-detail.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte';
    </script>

<main>
    <Navbar navLight={'nav-light'} logoLight={true} logoDark={false} />

    <section class="bg-half-170 d-table w-100"
        style={ `background-image: url(${imagebg}); background-position: top` }>
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row mt-5 justify-content-center">
                <div class="col-12">
                    <div class="title-heading text-center">
                        <span class="badge bg-primary">Jobnova</span>
                        <h5 class="heading fw-semibold mb-0 sub-heading text-white title-dark mt-4">Using Banner Stands To Increase Trade Show Traffic</h5>

                        <ul class="list-inline text-center mb-0">
                            <li class="list-inline-item mx-4 mt-4">
                                <span class="text-white-50 d-block">Author</span>
                                <a href="#name" class="text-white title-dark">Facebook</a>
                            </li>

                            <li class="list-inline-item mx-4 mt-4">
                                <span class="text-white-50 d-block">Date</span>
                                <span class="text-white title-dark">31st October 2023</span>
                            </li>

                            <li class="list-inline-item mx-4 mt-4">
                                <span class="text-white-50 d-block">Read Time</span>
                                <span class="text-white title-dark">8 min read</span>
                            </li>
                        </ul>
                    </div>
                </div><!--end col-->
            </div><!--end row-->

            <div class="position-middle-bottom">
                <nav aria-label="breadcrumb" class="d-block">
                    <ul class="breadcrumb breadcrumb-muted mb-0 p-0">
                        <li class="breadcrumb-item">
                            <Link to="/">Jobnova</Link>
                        </li>
                        <li class="breadcrumb-item">
                            <Link to="/blogs">Blogs</Link>
                        </li>
                        <li class="breadcrumb-item active" aria-current="page">Detail</li>
                    </ul>
                </nav>
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <Shape />

    <section class="section">
        <Detail />
    </section>
    <Footers explore={false} footerbar={false} />
    <Backtotop />

</main>

<style lang="scss" scoped></style>