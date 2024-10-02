<script>
    import { Link } from "svelte-routing";
    import Navbar from "../../components/navbar.svelte";
    import image from "../../assets/images/hero/bg.jpg";
    import Shape from "../../components/shape.svelte";
    import Questions from "../../components/helpcenter/faqs-questions.svelte";
    import Footers from "../../components/footer/footer.svelte";
    import Backtotop from "../../components/back-to-top.svelte";
</script>

<main>
    <Navbar navLight={"nav-light"} logoLight={true} />

    <section
        class="bg-half-170 d-table w-100"
        style={`background-image: url(${image}); background-position: top`}
    >
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row mt-5 justify-content-center">
                <div class="col-12">
                    <div class="title-heading text-center">
                        <h5
                            class="heading fw-semibold mb-0 sub-heading text-white title-dark"
                        >
                            Frequently Asked Questions
                        </h5>
                    </div>
                </div>
                <!--end col-->
            </div>
            <!--end row-->

            <div class="position-middle-bottom">
                <nav aria-label="breadcrumb" class="d-block">
                    <ul class="breadcrumb breadcrumb-muted mb-0 p-0">
                        <li class="breadcrumb-item">
                            <Link to="/">Jobnova</Link>
                        </li>
                        <li class="breadcrumb-item">
                            <Link to="/helpcenter-overview">Help Center</Link>
                        </li>
                        <li class="breadcrumb-item active" aria-current="page">
                            FAQs
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <!--end container-->
    </section>
    <!--end section-->
    <Shape />

    <section class="section">
        <Questions />
    </section>
    <Footers />
    <Backtotop />
</main>

<style lang="scss" scoped></style>
