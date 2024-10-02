<script>
    import ab01 from "../assets/images/about/ab01.jpg";
    import ab02 from "../assets/images/about/ab02.jpg";
    import {navigate} from 'svelte-routing'

    let toggle = true;
    const youtubeId = "yba7hPeTSjk";

    const datas = [
        "Digital Marketing Solutions for Tomorrow",
        "Our Talented & Experienced Marketing Agency",
        "Create your own skin to match your brand",
    ];

    function handler() {
        toggle = !toggle;
    }
</script>

<main>
    <div class="row g-4 align-items-center">
        <div class="col-lg-6 col-md-6 mb-5">
            <div class="about-left">
                <div class="position-relative shadow rounded img-one">
                    <img src={ab01} class="img-fluid rounded"  alt="" />
                </div>

                <div class="img-two shadow rounded p-2 bg-white">
                    <img src={ab02} class="img-fluid rounded" alt="" />
                    <div
                        class="position-absolute top-0 start-50 translate-middle"
                    >
                        <a href='#youtube' on:click|preventDefault={handler} data-type="youtube" data-id="yba7hPeTSjk" class="avatar avatar-md-md rounded-pill shadow card d-flex justify-content-center align-items-center lightbox" >
                            <i class="mdi mdi-play mdi-24px text-primary"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <!--end col-->

        <div class="col-lg-6 col-md-6">
            <div class="section-title ms-lg-5">
                <h4 class="title mb-3">
                    Millions of jobs. <br /> Find the one that's right for you.
                </h4>
                <p class="text-muted para-desc mb-0">
                    Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+
                    companies worldwide.
                </p>

                <ul class="list-unstyled text-muted mb-0 mt-3">
                    {#each datas as item}
                        <li class="mb-1">
                            <span class="text-primary h5 me-2">
                                <i
                                    class="mdi mdi-check-circle-outline align-middle"
                                ></i>
                            </span>
                            {item}
                        </li>
                    {/each}
                </ul>

                <div class="mt-4">
                    <a href="/aboutus" class="btn btn-primary" on:click={() => navigate('/aboutus')}>
                      About Us <i class="mdi mdi-arrow-right align-middle"></i>
                    </a>
                  </div>
            </div>
        </div>
        <!--end col-->
    </div>
    <!--end row-->

    {#if !toggle}
    <div class="modal-video" tabindex="-1" role="dialog" aria-modal="true" aria-label="You just opened the modal video" >
      <div class="modal-video-body">
        <div class="modal-video-inner">
          <div class="modal-video-movie-wrap">
            <iframe title="YouTube video player" width="460" height="230" src={`https://www.youtube.com/embed/${youtubeId}?feature=oembed`} frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" tabindex="-1" ></iframe>
            <a href="#video" on:click|preventDefault={handler} ><i class="mdi mdi-close m-3 h4 position-class title-icon"></i></a>
          </div>
        </div>
      </div>
    </div>
  {/if}
</main>

<style></style>
