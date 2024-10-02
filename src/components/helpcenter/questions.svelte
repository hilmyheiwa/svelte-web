<script>

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
    <div class="row justify-content-center">
        <div class="col-12">
            <div class="section-title text-center mb-4 pb-2">
                <h4 class="mb-4">Get Started</h4>
                <p class="para-desc mx-auto text-muted">We are a huge marketplace dedicated to connecting great artists
                    of all Jobnova with their fans and unique token collectors!</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row justify-content-center">
        <div class="col-lg-9 mt-4 pt-2">
            <div class="accordion" id="buyingquestion">
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
        </div><!--end col-->
    </div><!--end row-->
</main>

<style lang="scss" scoped></style>