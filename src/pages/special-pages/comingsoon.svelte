<script>
    import { Link } from 'svelte-routing';
    import image from '../../assets/images/hero/bg2.jpg';
    import logo from '../../assets/images/logo-icon-80-white.png'
    
    import { onMount } from 'svelte';

  let date = new Date().getFullYear();
  let now = new Date().getTime();
  let targetTime = new Date("Sep 26, 2025 00:00:00").getTime();
  let difference = 0;

  $: days = Math.floor(difference / (1000 * 60 * 60 * 24));
  $: hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  $: minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
  $: seconds = Math.floor((difference % (1000 * 60)) / 1000);

  onMount(() => {
    updateNow();
    setInterval(updateNow, 1000);
  });

  function updateNow() {
    now = new Date().getTime();
    difference = targetTime - now;
  }
    </script>

<main>
    <section class="bg-home d-flex align-items-center"
        style={ `background-image: url(${image}); background-position: top` }>
        <div class="bg-overlay bg-gradient-overlay"></div>
        <div class="container">
            <div class="row">
                <div class="col-12 p-0">
                    <div class="d-flex flex-column min-vh-100 justify-content-center p-md-5">
                        <div class="text-center">
                            <Link to="/"><img src={logo} alt=""></Link>
                        </div>
                        <div class="title-heading text-center my-auto">
                            <h2 class="title-dark text-white text-uppercase mt-2 mb-4 fw-semibold">We are coming soon...
                            </h2>
                            <p class="text-white para-desc para-dark mx-auto">Find Jobs, Employment & Career
                                Opportunities. Some of the companies we've helped recruit excellent applicants over the
                                years.</p>

                            <div id="countdown">
                                <ul class="count-down list-unstyled">
                                    <li id="days" class="count-number list-inline-item m-2">{ days }<p
                                            class="count-head">Days
                                        </p>
                                    </li>
                                    <li id="hours" class="count-number list-inline-item m-2">{ hours }<p
                                            class="count-head">
                                            Hours</p>
                                    </li>
                                    <li id="mins" class="count-number list-inline-item m-2">{ minutes }<p
                                            class="count-head">
                                            minutes</p>
                                    </li>
                                    <li id="secs" class="count-number list-inline-item m-2">{ seconds }<p
                                            class="count-head">
                                            seconds</p>
                                    </li>
                                    <li id="end" class="h1"></li>
                                </ul>
                            </div>
                        </div>
                        <div class="text-center">
                            <p class="mb-0 text-white-50">©
                                { date } Jobnova. Design & Develop with <i class="mdi mdi-heart text-danger"></i> by
                                <a href="https://shreethemes.in/" target="_blank" class="text-reset">Shreethemes</a>.
                            </p>
                        </div>
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div><!--end container-->
    </section><!--end section-->
</main>

<style lang="scss" scoped></style>