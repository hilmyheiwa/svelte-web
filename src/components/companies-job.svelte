<script>
import image from '../assets/images/company/facebook-logo.png';
import image2 from '../assets/images/company/google-logo.png';
import image3 from '../assets/images/company/android.png';
import image4 from '../assets/images/company/lenovo-logo.png';
import image5 from '../assets/images/company/spotify.png';
import image6 from '../assets/images/company/linkedin.png';
import image7 from '../assets/images/about/ab03.jpg';
import image8 from '../assets/images/about/ab04.jpg';
import {navigate} from 'svelte-routing'

let toggle = true;
    const youtubeId = "yba7hPeTSjk";

const jobData = [
      {
          id: 1,
          image: image,
          name: 'Facebook',
          vacancy: '10 vacancy',
      },
      {
          id: 2,
          image: image2,
          name: 'Google',
          vacancy: '10 vacancy',
      },
      {
          id: 3,
          image: image3,
          name: 'Android',
          vacancy: '10 vacancy',
      },
      {
          id: 4,
          image: image4,
          name: 'Lenovo',
          vacancy: '10 vacancy',
      },
      {
          id: 5,
          image: image5,
          name: 'Spotify',
          vacancy: '10 vacancy',
      },
      {
          id: 6,
          image: image6,
          name: 'Linkedin',
          vacancy: '10 vacancy',
      },
  ]
  
  function handler() {
        toggle = !toggle;
    }
  
  </script>
  
  
  
  <main>
    <div class="row g-4 align-items-center">
        <div class="col-lg-6 col-md-6 mb-5  order-md-2 order-1">
            <div class="about-right">
                <div class="position-relative shadow rounded img-one">
                    <img src={image7} class="img-fluid rounded" alt="">
                </div>

                <div class="img-two shadow rounded p-2 bg-white">
                    <img src={image8} class="img-fluid rounded" alt="">

                    <div class="position-absolute top-0 start-50 translate-middle">
                        <a href='#youtube' on:click|preventDefault={handler} data-type="youtube" data-id="yba7hPeTSjk"
                            class="avatar avatar-md-md rounded-pill shadow card d-flex justify-content-center align-items-center lightbox">
                            <i class="mdi mdi-play mdi-24px text-primary"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div><!--end col-->

        <div class="col-lg-6 col-md-6 mt-4 pt-2 mt-sm-0 pt-sm-0 order-md-1 order-2">
            <div class="section-title mb-4 me-lg-5">
                <h4 class="title mb-3">Find Best Companies.</h4>
                <p class="text-muted para-desc mb-0">Search all the open positions on the web. Get your own personalized
                    salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>

            <div class="row g-4 mt-0">
                {#each jobData as item }
                <div class="col-md-6">
                    <div class="employer-card rounded shadow p-2 bg-light">
                        <div class="d-flex align-items-center">
                            <img src={item.image}
                                class="avatar avatar-md-sm rounded shadow p-2 bg-white" alt="">

                            <div class="content ms-3">
                                <a href={`/employer-profile/${item.id}`} class="h5 title text-dark">{ item.name
                                    }</a>
                                <span class="text-muted d-flex align-items-center small mt-1">{ item.vacancy }</span>
                            </div>
                        </div>
                    </div>
                </div>
                {/each}
            </div>

            <div class="mt-4">
                <a href="/employers" class="btn btn-link primary text-muted" on:click={() => navigate('/employers')}>See More Companies <i
                        class="mdi mdi-arrow-right align-middle"></i></a>
            </div>
        </div><!--end col-->
    </div><!--end row-->

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


<style lang="scss" scoped></style>