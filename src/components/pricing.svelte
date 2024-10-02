<script>
    
    const datas = [
        {
            name: 'Starter',
            title: 'Suitable for Starter',
            price: '0.00',
            feature: ['Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Free Appointments', 'Free Installment'],
            button: 'Free Signup',
            text: 'dark',
            number: '4'
        },
        {
            name: 'Professional',
            title: 'Suitable for Regular',
            price: '9.99',
            feature: ['Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Free Appointments', 'Free Installment'],
            button: 'Subscribe Now',
            text: 'dark',
            number: '4'
        },
        {
            name: 'Standerd',
            title: 'Suitable for Business',
            price: '19.99',
            feature: ['Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Free Appointments', 'Free Installment'],
            button: 'Buy Now',
            text: 'primary',
            number: '5'
        },
        {
            name: 'Premium',
            title: 'Suitable for Premium',
            price: '29.99',
            feature: ['Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Free Appointments', 'Free Installment'],
            button: 'Buy Premium',
            class: 'price-header rounded-top bg-dark bg-white-dark pt-5 pb-5',
            text: 'dark',
            number: '4'
        },
    ]
    </script>

<main>
    <div class="container">
        <div class="row g-4 align-items-lg-center">

            {#each datas as item, index}
            <div class="col-lg-3 col-md-6 col-12">
              <div
                class={
                  index === 2
                    ? 'pricing text-center rounded position-relative shadow-lg bg-light'
                    : 'pricing text-center rounded position-relative overflow-hidden shadow'
                }
              >
                {#if index === 1}
                  <div class="ribbon ribbon-right overflow-hidden">
                    <span class="text-center bg-warning d-block shadow small h6">Best</span>
                  </div>
                {/if}
                <div
                  class={
                    index === 2
                      ? 'price-header rounded-top bg-primary pt-5 pb-5'
                      : 'price-header rounded-top bg-dark bg-white-dark pt-5 pb-5'
                  }
                >
                  <h5 class="price-title text-white title-dark">{item.name}</h5>
                  <p class="mb-0 text-white-50">{item.title}</p>
                </div>
                <div class={`d-flex justify-content-center bg-light border-bottom py-${item.number}`}>
                  <span class="h6 mb-0">$</span>
                  <span class="price h4 mb-0 ms-1">{item.price}</span>
                  <span class="h6 align-self-end mb-1">/mo</span>
                </div>
                <div class="pricing-features text-start">
                  <ul class="feature list-unstyled py-4 p-3 mb-0">
                    {#each item.feature as feature, featureIndex}
                      <li class={featureIndex > 0 ? 'feature-list text-muted mt-2' : 'feature-list text-muted'}>
                        <i
                          data-feather="arrow-right-circle"
                          class={`fea icon-sm text-${item.text} me-2`}
                        ></i>
                        {feature}
                      </li>
                    {/each}
                  </ul>
                  <div class={`border-top text-center py-${item.number}`}>
                    <a href="#name" class={`btn btn-${item.text}`}>{item.button}</a>
                  </div>
                </div>
              </div>
            </div>
          {/each}


        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>