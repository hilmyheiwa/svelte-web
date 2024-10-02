<script>
    import image from '../assets/images/about/ab01.jpg';
    import imagetwo from '../assets/images/about/ab02.jpg';

    let toggle = true;
        const youtubeId = "yba7hPeTSjk";
        
        function handler() {
            toggle = !toggle;
        }
    
    const datas = [
        {
            id: "headingOne",
            collapseId: "collapseOne",
            question: "How does it work ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: true
        },
        {
            id: "headingTwo",
            collapseId: "collapseTwo",
            question: "Do I need a designer to use Jobnova ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingThree",
            collapseId: "collapseThree",
            question: "What do I need to do to start selling ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingFour",
            collapseId: "collapseFour",
            question: "What happens when I receive an order ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        }
    ]
    
    </script>

<main>
    <div class="row g-4 align-items-center">
        <div class="col-lg-6 col-md-6 mb-5">
            <div class="about-left">
                <div class="position-relative shadow rounded img-one">
                    <img src={image} class="img-fluid rounded" alt="">
                </div>

                <div class="img-two shadow rounded p-2 bg-white">
                    <img src={imagetwo} class="img-fluid rounded" alt="">

                    <div class="position-absolute top-0 start-50 translate-middle">
                        <a href="#youtube" on:click|preventDefault={handler} data-type="youtube" data-id="yba7hPeTSjk" class="avatar avatar-md-md rounded-pill shadow card d-flex justify-content-center align-items-center lightbox">
                            <i class="mdi mdi-play mdi-24px text-primary"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div><!--end col-->

        <div class="col-lg-6 col-md-6">
            <div class="section-title mb-4 ms-lg-3">
                <h4 class="title mb-3">Frequently Asked Questions</h4>
                <p class="text-muted para-desc mb-0">Search all the open positions on the web. Get your own personalized
                    salary estimate. Read reviews on over 30000+ companies worldwide.</p>

                    <div class="accordion mt-4 pt-2" id="buyingquestion">
                        {#each datas as item, index}
                          <div class={`accordion-item rounded ${index > 0? 'mt-2' : ''}`}>
                            <h2 class="accordion-header" id={item.id}>
                              <button
                                class={`accordion-button border-0 bg-light ${item.show? '' : 'collapsed'}`}
                                type="button"
                                data-bs-toggle="collapse"
                                data-bs-target={`#${item.collapseId}`}
                                aria-expanded={item.show? 'true' : 'false'}
                                aria-controls={item.collapseId}
                              >
                                {item.question}
                              </button>
                            </h2>
                            <div
                              id={item.collapseId}
                              class={`accordion-collapse border-0 collapse ${item.show? 'show' : ''}`}
                              aria-labelledby="headingOne"
                              data-bs-parent="#buyingquestion"
                            >
                              <div class="accordion-body text-muted">
                                {item.answer}
                              </div>
                            </div>
                          </div>
                        {/each}
                      </div>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    {#if !toggle}
    <div
        class="modal-video"
        tabindex="-1"
        role="dialog"
        aria-modal="true"
        aria-label="You just opened the modal video"
    >
        <div class="modal-video-body">
            <div class="modal-video-inner">
                <div class="modal-video-movie-wrap">
                    <iframe
                        title="YouTube video player"
                        width="460"
                        height="230"
                        src={`https://www.youtube.com/embed/${youtubeId}?feature=oembed`}
                        frameborder="0"
                        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                        tabindex="-1"
                    ></iframe>
                    <a href="#video" on:click|preventDefault={handler}
                        ><i
                            class="mdi mdi-close m-3 h4 position-class title-icon"
                        ></i></a
                    >
                </div>
            </div>
        </div>
    </div>
{/if}
</main>

<style lang="scss" scoped></style>