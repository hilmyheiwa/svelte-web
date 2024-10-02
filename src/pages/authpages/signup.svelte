<script>
    import image from '../../assets/images/hero/bg3.jpg';
    import { Link } from 'svelte-routing';
    import logo from '../../assets/images/logo-dark.png'
    
    </script>

<main>
    <section class="bg-home d-flex align-items-center" style={ `background-image: url(${image})` }>
        <div class="bg-overlay bg-linear-gradient-2"></div>
        <div class="container">
            <div class="row">
                <div class="col-lg-4 col-md-5 col-12">
                    <div class="p-4 bg-white rounded shadow-md mx-auto w-100" style="max-width: 400px;">
                        <form>
                            <Link to="/"><img src={logo}
                                    class="mb-4 d-block mx-auto" alt=""></Link>
                            <h6 class="mb-3 text-uppercase fw-semibold">Register your account</h6>

                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="name">Your Name</label>
                                <input name="name" id="name" type="text" class="form-control"
                                    placeholder="Calvin Carlo">
                            </div>

                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="email">Your Email</label>
                                <input name="email" id="email" type="email" class="form-control"
                                    placeholder="example@website.com">
                            </div>

                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="loginpass">Password</label>
                                <input type="password" class="form-control" id="loginpass" placeholder="Password">
                            </div>

                            <div class="form-check mb-3">
                                <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
                                <label class="form-label form-check-label text-muted" for="flexCheckDefault">I Accept <a
                                        href="#name" class="text-primary">Terms And Condition</a></label>
                            </div>

                            <button class="btn btn-primary w-100" type="submit">Register</button>

                            <div class="col-12 text-center mt-3">
                                <span><span class="text-muted small me-2">Already have an account ? </span> <Link
                                        to="/login" class="text-dark fw-semibold small">Sign in</Link></span>
                            </div><!--end col-->
                        </form>
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div><!--end container-->
    </section><!--end section-->
</main>


<style lang="scss" scoped></style>