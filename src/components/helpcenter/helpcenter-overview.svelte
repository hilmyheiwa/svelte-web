<script>
    import { Link } from "svelte-routing";

    const datas = [
        {
            icon: 'help-circle',
            link: '/helpcenter-faqs',
            name: 'FAQs',
            title: 'The phrasal sequence of the is now so that many campaign and benefit'
        },
        {
            icon: 'bookmark',
            link: '/helpcenter-guides',
            name: 'Guides / Support',
            title: 'The phrasal sequence of the is now so that many campaign and benefit'
        },
        {
            icon: 'settings',
            link: '/helpcenter-support',
            name: 'Support Request',
            title: 'The phrasal sequence of the is now so that many campaign and benefit'
        },
    ]
    
    </script>

<main>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-12">
                <div class="section-title text-center mb-4 pb-2">
                    <h4 class="mb-4 title">Find the help you need</h4>
                    <p class="para-desc mx-auto text-muted">We are a huge marketplace dedicated to connecting great
                        artists of all Jobnova with their fans and unique token collectors!</p>
                </div>
            </div><!--end col-->
        </div><!--end row-->

        <div class="row justify-content-center">
            {#each datas as item}
            <div class="col-md-4 mt-4 pt-2">
                <div class="position-relative features text-center mx-lg-4 px-md-1">
                    <div
                        class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
                        <i data-feather={item.icon} class="fea icon-ex-md"></i>
                    </div>

                    <div class="mt-4">
                        <Link to={item.link} class="title h5 text-dark">{item.name}</Link>
                        <p class="text-muted mt-3 mb-0">{ item.title }</p>
                        <div class="mt-3">
                            <Link to={item.link} class="btn btn-link primary text-primary">Read More <i
                                    class="mdi mdi-arrow-right"></i></Link>
                        </div>
                    </div>
                </div>
            </div><!--end col-->
            {/each}
           
        </div><!--end row-->
    </div><!--end container-->
</main>


<style lang="scss" scoped></style>