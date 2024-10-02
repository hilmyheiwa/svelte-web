<script>
    import Navbar from '../../components/navbar.svelte';
    import Shape from '../../components/shape.svelte';
    import image from '../../assets/images/hero/bg.jpg';
    import Overview from '../../components/helpcenter/helpcenter-overview.svelte';
    import Questions from '../../components/helpcenter/questions.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte';
    import { Link } from 'svelte-routing';
    
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
                        <h5 class="heading fw-semibold mb-0 sub-heading text-white title-dark">Hello! <br> How can we
                            help you?</h5>
                    </div>

                    <div class="subscribe-form mt-4">
                        <form class="mx-auto" action="/">
                            <input type="text" id="help" name="name" class="rounded-pill bg-white-50" required=""
                                placeholder="Search your questions or topic...">
                            <button type="submit" class="btn btn-primary rounded-pill">Search</button>
                        </form>
                    </div>
                </div><!--end col-->
            </div><!--end row-->

            <div class="position-middle-bottom">
                <nav aria-label="breadcrumb" class="d-block">
                    <ul class="breadcrumb breadcrumb-muted mb-0 p-0">
                        <li class="breadcrumb-item">
                            <Link to="/">Jobnova</Link>
                        </li>
                        <li class="breadcrumb-item active" aria-current="page">Helpcenter</li>
                    </ul>
                </nav>
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <Shape />

    <section class="section">
        <Overview />
        <div class="container mt-100 mt-60">
            <Questions />
        </div>
    </section>
    <Footers />
    <Backtotop />
</main>

<style lang="scss" scoped></style>