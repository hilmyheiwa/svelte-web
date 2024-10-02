<script>
    import { onMount } from 'svelte';
    
    let activeId = ('')
    
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
    
    const generalquestion = [
        {
            id: "headingThirteen",
            collapseId: "collapseThirteen",
            question: "How does it work ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: true
        },
        {
            id: "headingfourteen",
            collapseId: "collapsefourteen",
            question: "Do I need a designer to use Jobnova ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingfifteen",
            collapseId: "collapsefifteen",
            question: "What do I need to do to start selling ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingSixteen",
            collapseId: "collapseSixteen",
            question: "What happens when I receive an order ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        }
    ]
    
    const paymentquestion = [
        {
            id: "headingFive",
            collapseId: "collapseFive",
            question: "How does it work ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: true
        },
        {
            id: "headingSix",
            collapseId: "collapseSix",
            question: "Do I need a designer to use Jobnova ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingSeven",
            collapseId: "collapseSeven",
            question: "What do I need to do to start selling ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingEight",
            collapseId: "collapseEight",
            question: "What happens when I receive an order ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        }
    ]
    
    const supportquestion = [
        {
            id: "headingNine",
            collapseId: "collapseNine",
            question: "How does it work ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: true
        },
        {
            id: "headingTen",
            collapseId: "collapseTen",
            question: "Do I need a designer to use Jobnova ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingEleven",
            collapseId: "collapseEleven",
            question: "What do I need to do to start selling ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        },
        {
            id: "headingTwelve",
            collapseId: "collapseTwelve",
            question: "What happens when I receive an order ?",
            answer: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.",
            show: false,
        }
    ]

    onMount(() => {
        window.addEventListener('scroll', checkVisibleDiv);
    })
    
    function checkVisibleDiv() {
        const windowHeight = window.innerHeight;
        const divElements = document.querySelectorAll('.scroll-div');
        divElements.forEach(div => {
            const rect = div.getBoundingClientRect();
            const isVisible = (rect.top <= 300 && rect.bottom <= windowHeight);
            if (isVisible) {
                activeId = div.id;
            }
        });
    }
    
    
    </script>

<main>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-4 col-md-5 col-12 d-none d-md-block">
                <div class="rounded shadow p-4 sticky-bar">
                    <ul class="list-unstyled sidebar-nav mb-0 py-0" id="navmenu-nav">
                        {#if activeId === 'tech'}
                          <li class="navbar-item p-0 active">
                            <a href="#tech" class="h6 text-dark navbar-link">Buying Questions</a>
                          </li>
                        {:else}
                          <li class="navbar-item p-0">
                            <a href="#tech" class="h6 text-dark navbar-link">Buying Questions</a>
                          </li>
                        {/if}
                      
                        {#if activeId === 'general'}
                          <li class="navbar-item mt-3 p-0 active">
                            <a href="#general" class="h6 text-dark navbar-link">General Questions</a>
                          </li>
                        {:else}
                          <li class="navbar-item mt-3 p-0">
                            <a href="#general" class="h6 text-dark navbar-link">General Questions</a>
                          </li>
                        {/if}
                      
                        {#if activeId === 'payment'}
                          <li class="navbar-item mt-3 p-0 active">
                            <a href="#payment" class="h6 text-dark navbar-link">Payments Questions</a>
                          </li>
                        {:else}
                          <li class="navbar-item mt-3 p-0">
                            <a href="#payment" class="h6 text-dark navbar-link">Payments Questions</a>
                          </li>
                        {/if}
                      
                        {#if activeId === 'support'}
                          <li class="navbar-item mt-3 p-0 active">
                            <a href="#support" class="h6 text-dark navbar-link">Support Questions</a>
                          </li>
                        {:else}
                          <li class="navbar-item mt-3 p-0">
                            <a href="#support" class="h6 text-dark navbar-link">Support Questions</a>
                          </li>
                        {/if}
                      </ul>
                </div>
            </div><!--end col-->

            <div class="col-lg-8 col-md-7 col-12">
                <div class="section-title scroll-div"  id="tech">
                    <h4>Buying Product</h4>
                </div>

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

                <div class="section-title mt-5 scroll-div" id="general">
                    <h4>General Questions</h4>
                </div>

                <div class="accordion mt-4 pt-2" id="generalquestion">
                    {#each generalquestion as item, index}
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

                <div class="section-title mt-5 scroll-div" id="payment">
                    <h4>Payments Questions</h4>
                </div>

                <div class="accordion mt-4 pt-2" id="paymentquestion">
                    {#each paymentquestion as item, index}
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

                <div class="section-title mt-5 scroll-div" id="support">
                    <h4>Support Questions</h4>
                </div>

                <div class="accordion mt-4 pt-2" id="supportquestion">
                    {#each supportquestion as item, index}
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
    </div><!--end container-->
</main>


<style lang="scss" scoped></style>