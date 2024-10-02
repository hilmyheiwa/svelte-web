<script>
    import image from '../../assets/images/hero/bg2.jpg';
    import logo from '../../assets/images/logo-icon-80-white.png';
    import { Link } from 'svelte-routing';
    import { onMount } from 'svelte'
    
    let timer = (60 * 60) // 1 hour in seconds
    let minutes = ('')
    let seconds = ('')
    
    onMount(() => {
        const display = document.querySelector('#maintenance')
        setInterval(() => {
            minutes = String(Math.floor(timer / 60)).padStart(2, '0')
            seconds = String(timer % 60).padStart(2, '0')
            display.textContent = `${minutes}:${seconds}`
            timer--
            if (timer < 0) {
                timer = 60 * 60
            }
        }, 1000)
    })
    </script>

<main>
    <section class="bg-home d-flex align-items-center" style={
        `background-image: url(${image}); background-position: top`
    }>
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-12 text-center">
                    <Link to="/">
                        <img src={logo} alt="">
                    </Link>
                    <h2 class="title-dark text-white text-uppercase mt-2 mb-4 fw-semibold">We are back soon...</h2>
                    <p class="text-white-50 para-desc para-dark mx-auto">Find Jobs, Employment & Career Opportunities.
                        Some of the companies we've helped recruit excellent applicants over the years.</p>
                </div><!--end col-->
            </div><!--end row-->

            <div class="row">
                <div class="col-md-12 text-center">
                    <div class="text-center">
                        <span id="maintenance" class="timer"></span><span
                            class="d-block h6 text-uppercase text-white title-dark">Minutes</span>
                    </div>
                </div>
            </div>

            <div class="row mt-4 pt-2">
                <div class="col-12 text-center">
                    <div class="subscribe-form">
                        <form class="mx-auto" action="/">
                            <input name="email" id="email" type="email" class="rounded-pill bg-white" required
                                placeholder="Your email :">
                            <button type="submit" class="btn btn-primary rounded-pill">Subscribe</button>
                        </form>
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div>
    </section>
</main>

<style lang="scss" scoped></style>