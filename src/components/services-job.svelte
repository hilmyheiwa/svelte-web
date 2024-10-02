<script>
    export let information ;
   export let services ;
    let datas = [
        {
            icon: 'phone',
            name: '24/7 Support',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'cpu',
            name: 'Tech & Startup Jobs',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'activity',
            name: 'Quick & Easy',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'clock',
            name: 'Save Time',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'file-text',
            name: 'Apply with confidence',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'codesandbox',
            name: 'Reduce Hiring Bias',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'users',
            name: 'Proactive Employers',
            title: 'Many desktop publishing now use and a search for job.'
        },
        {
            icon: 'user-check',
            name: 'No Missed Opportunities',
            title: 'Many desktop publishing now use and a search for job.'
        },
    ];
</script>

{#if information}
<div class="row justify-content-center mb-4 pb-2">
    <div class="col-12">
        <div class="section-title text-center">
            <h4 class="title mb-3">Here's why you'll love it Jobnova</h4>
            <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
        </div>
    </div><!--end col-->
</div><!--end row-->
{/if}

{#if services}
<div class="row">
    {#each datas as item}
    <div class="col-lg-3 col-md-4 col-sm-6 col-12 mt-4 pt-2">
        <div class="position-relative features text-center p-4 rounded shadow bg-white">
            <div class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
                <i data-feather={item.icon} class="fea icon-ex-md"></i>
            </div>

            <div class="mt-4">
                <a href="#name" class="title h5 text-dark">{item.name}</a>
                <p class="text-muted mt-3 mb-0">{item.title}</p>
                <div class="mt-3">
                    <a href="#read" class="btn btn-link primary text-dark">Read More <i class="mdi mdi-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </div><!--end col-->
    {/each}
</div><!--end row-->

{:else}
<div class="row">
    {#each datas.slice(0, 4) as item}
    <div class="col-lg-3 col-md-4 col-sm-6 col-12 mt-4 pt-2">
        <div class="position-relative features text-center p-4 rounded shadow bg-white">
            <div class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
                <i data-feather={item.icon} class="fea icon-ex-md"></i>
            </div>

            <div class="mt-4">
                <a href="#name" class="title h5 text-dark">{item.name}</a>
                <p class="text-muted mt-3 mb-0">{item.title}</p>
                <div class="mt-3">
                    <a href="#read" class="btn btn-link primary text-dark">Read More <i class="mdi mdi-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </div><!--end col-->
    {/each}
</div><!--end row-->
{/if}

<style lang="scss">
    /* Add your styles here */
</style>