<script>
    
    let isActive = (true);
    
    let toggle = () => {
        isActive = !isActive;
    }
    
    const contactInfo = [
        {
            icon: 'phone',
            title: 'Phone',
            description: 'Start working with Landflow that can provide everything',
            href: 'tel:+152534-468-854',
            linkText: '+152 534-468-854'
        },
        {
            icon: 'mail',
            title: 'Email',
            description: 'Start working with Landflow that can provide everything',
            href: 'mailto:contact@example.com',
            linkText: 'contact@example.com'
        },
    ]
    </script>

<main>
    <div class="row">
        {#each contactInfo as item, index}
        <div class={`col-md-4 ${index === 1 ? 'mt-lg-0 mt-4' : ''}`}>
            <div class="position-relative features text-center mx-lg-4 px-md-1">
                <div
                    class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
                    <i data-feather={item.icon} class="fea icon-ex-md"></i>
                </div>

                <div class="mt-4">
                    <h5 class="mb-3">{ item.title }</h5>
                    <p class="text-muted">{ item.description }</p>
                    <a href={item.href} class="text-primary">{ item.linkText }</a>
                </div>
            </div>
        </div><!--end col-->
        {/each}
      

        <div class="col-md-4 mt-lg-0 mt-4">
            <div class="position-relative features text-center mx-lg-4 px-md-1">
                <div
                    class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
                    <i data-feather="map-pin" class="fea icon-ex-md"></i>
                </div>

                <div class="mt-4">
                    <h5 class="mb-3">Location</h5>
                    <p class="text-muted">C/54 Northwest Freeway, Suite 558, <br>Houston, USA 485</p>
                    <a on:click={toggle} class="text-primary lightbox">View on Google map</a>
                </div>
            </div>
        </div><!--end col-->
    </div>

    {#if !isActive}
    <div class="modal-video" tabindex="-1" role="dialog" aria-modal="true"
    aria-label="You just opened the modal video">
    <div class="modal-video-body">
        <div class="modal-video-inner">
            <div class="modal-video-movie-wrap">
                <iframe width="460" height="230" title="map"
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                    frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen tabindex="-1">
                </iframe>
                <a on:click|preventDefault={toggle} class="mdi mdi-close m-3 h4 position-class title-icon"> </a>
            </div>
        </div>
    </div>
</div>
    {/if}
   
</main>

<style lang="scss" scoped>
/* your styles here */
</style>