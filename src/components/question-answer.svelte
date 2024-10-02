<script>
    
    const datas = [
        {
            que: 'How our',
            quetwo: 'Jobnova',
            quethree: 'work ?',
            answer: 'Due to its widespread use as filler text for layouts, non- readability is of great importance: human perception is tuned to recognize certain patterns and repetitions in texts.',
        },
        {
            que: 'What is the main process open account ?',
            quetwo: '',
            quethree: '',
            answer: 'Furthermore, it is advantageous when the dummy text is relatively realistic so that the layout impression of the final publication is not compromised.',
        },
        {
            que: 'How to make unlimited data entry ?',
            quetwo: '',
            quethree: '',
            answer: "If the distribution of letters and 'words' is random, the reader will not be distracted from making a neutral judgement on the visual impact",
        },
        {
            que: 'Is',
            quetwo: 'Jobnova',
            quethree: 'safer to use with my account ?',
            answer: "The most well-known dummy text is the 'Lorem Ipsum', which is said to have originated in the 16th century. Lorem Ipsum is composed in a pseudo-Latin language which more or less corresponds to 'proper' Latin.",
        },
    ]
    </script>

<main>
    <div class="row justify-content-center">
        <div class="col">
            <div class="section-title text-center mb-4 pb-2">
                <h4 class="title mb-3">Questions & Answers</h4>
                <p class="text-muted para-desc mb-0 mx-auto">Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row mt-4 pt-2">
        {#each datas as item, index}
        <div class={`col-md-6 col-12 ${index > 0? 't-4 pt-2' : ''} ${index === 1? 't-sm-0 pt-sm-0' : ''}`}>
          <div class="d-flex">
            <i data-feather="help-circle" class="fea icon-ex-md text-primary me-2 mt-1"></i>
            <div class="flex-1">
              <h5 class="mt-0">{item.que} <span class="text-primary">{item.quetwo}</span> {item.quethree}</h5>
              <p class="answer text-muted mb-0">{item.answer}</p>
            </div>
          </div>
        </div>
        {/each}
      </div>
</main>

<style lang="scss" scoped></style>