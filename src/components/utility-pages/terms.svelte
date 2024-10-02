<script>

    const digital = ['Digital Marketing Solutions for Tomorrow', 'Our Talented & Experienced Marketing Agency', 'Create your own skin to match your brand', 'Digital Marketing Solutions for Tomorrow', 'Our Talented & Experienced Marketing Agency', 'Create your own skin to match your brand']
    
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
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-9">
                <div class="card shadow border-0 rounded">
                    <div class="card-body">
                        <h5 class="card-title">Introduction :</h5>
                        <p class="text-muted">It seems that only fragments of the original text remain in the Lorem
                            Ipsum texts used today. One may speculate that over the course of time certain letters were
                            added or deleted at various positions within the text.</p>

                        <h5 class="card-title">User Agreements :</h5>
                        <p class="text-muted">The most well-known dummy text is the 'Lorem Ipsum', which is said to have
                            <b class="text-danger">originated</b> in the 16th century. Lorem Ipsum is <b
                                class="text-danger">composed</b> in a pseudo-Latin language which more or less <b
                                class="text-danger">corresponds</b> to 'proper' Latin. It contains a series of real
                            Latin words. This ancient dummy text is also <b class="text-danger">incomprehensible</b>,
                            but it imitates the rhythm of most European languages in Latin script. The <b
                                class="text-danger">advantage</b> of its Latin origin and the relative <b
                                class="text-danger">meaninglessness</b> of Lorum Ipsum is that the text does not attract
                            attention to itself or distract the viewer's <b class="text-danger">attention</b> from the
                            layout.
                        </p>
                        <p class="text-muted">There is now an <b class="text-danger">abundance</b> of readable dummy
                            texts. These are usually used when a text is <b class="text-danger">required purely</b> to
                            fill a space. These alternatives to the classic Lorem Ipsum texts are often amusing and tell
                            short, funny or <b class="text-danger">nonsensical</b> stories.</p>
                        <p class="text-muted">It seems that only <b class="text-danger">fragments</b> of the original
                            text remain in the Lorem Ipsum texts used today. One may speculate that over the course of
                            time certain letters were added or deleted at various positions within the text.</p>

                        <h5 class="card-title">Restrictions :</h5>
                        <p class="text-muted">You are specifically restricted from all of the following :</p>
                        <ul class="list-unstyled text-muted">
                            {#each digital as item}
                            <li  class="mt-2"><i data-feather="arrow-right"
                                    class="fea icon-sm me-2"></i>{ item }</li>                                
                            {/each}
                        </ul>

                        <h5 class="card-title">Users Question & Answer :</h5>

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

                        <div class="mt-3">
                            <a href="#name" class="btn btn-primary mt-2 me-2">Accept</a>
                            <a href="#name" class="btn btn-outline-primary mt-2">Decline</a>
                        </div>
                    </div>
                </div>
            </div><!--end col-->
        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>