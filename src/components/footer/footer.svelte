<script>
	import { Link } from 'svelte-routing';
    import image from '../../assets/images/logo-light.png'

    export let explore;
      export let footerbar;
   
   const datas = [
       {
           link: '/',
           name: 'Home'
       },
       {
           link: '/services',
           name: 'How it works'
       },
       {
           link: '/job-post',
           name: 'Create a job'
       },
       {
           link: '/aboutus',
           name: 'About us'
       },
       {
           link: '/pricing',
           name: 'Plans'
       },
   ]
   
   const social = [
       {
           link: 'https://dribbble.com/shreethemes',
           icon: 'dribbble'
       },
       {
           link: 'http://linkedin.com/company/shreethemes',
           icon: 'linkedin'
       },
       {
           link: 'https://www.facebook.com/shreethemes',
           icon: 'facebook'
       },
       {
           link: 'https://www.instagram.com/shreethemes/',
           icon: 'instagram'
       },
       {
           link: 'https://twitter.com/shreethemes',
           icon: 'twitter'
       },
   ]
   
   const date = (new Date().getFullYear())
   </script>

<main>
    <!-- Footer Start -->
    <footer class="bg-footer">
        {#if explore}
            
        <div class="py-5">
            <div class="container">
                <div class="row align-items-end">
                    <div class="col-md-7">
                        <div class="section-title">
                            <div class="d-flex align-items-center">
                                <i data-feather="bookmark" class="fea icon-lg"></i>
                                <div class="flex-1 ms-3">
                                    <h4 class="fw-bold text-white mb-2">Explore a job now!</h4>
                                    <p class="text-white-50 mb-0">Search all the open positions on the web. Get your own
                                        personalized salary estimate. Read reviews on over 30000+ companies worldwide.
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div><!--end col-->

                    <div class="col-md-5 mt-4 mt-sm-0">
                        <div class="text-md-end ms-5 ms-sm-0">
                            <Link to="/job-apply" class="btn btn-primary me-1 my-1">Apply Now</Link>
                            <Link to="/contactus" class="btn btn-soft-primary my-1">Contact Us</Link>
                        </div>
                    </div><!--end col-->
                </div><!--end row-->
            </div><!--end container-->
        </div><!--end div-->

        {/if}
        
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class={`py-5 ${footerbar}`}>
                        <div class="row align-items-center">
                            <div class="col-sm-3">
                                <div class="text-center text-sm-start">
                                    <a href="#name"><img src={image} alt=""></a>
                                </div>
                            </div>

                            <div class="col-sm-9 mt-4 mt-sm-0">
                                <ul class="list-unstyled footer-list terms-service text-center text-sm-end mb-0">
                                    {#each datas as item}
                                    <li class="list-inline-item my-2"><Link
                                            to={item.link} class="text-foot fs-6 fw-medium me-2"><i
                                                class="mdi mdi-circle-small"></i>
                                            { item.name }</Link></li>                                        
                                    {/each}
                                </ul>
                            </div><!--end col-->
                        </div><!--end row-->
                    </div>
                </div><!--end col-->
            </div><!--end row-->
        </div><!--end container-->

        <div class="py-4 footer-bar">
            <div class="container text-center">
                <div class="row align-items-center">
                    <div class="col-sm-6">
                        <div class="text-sm-start">
                            <p class="mb-0 fw-medium">©
                                { date } Jobnova. Design & Develop with <i class="mdi mdi-heart text-danger"></i> by
                                <a href="https://shreethemes.in/" target="_blank" class="text-reset">Shreethemes</a>.
                            </p>
                        </div>
                    </div>

                    <div class="col-sm-6 mt-4 mt-sm-0 pt-2 pt-sm-0">
                        <ul class="list-unstyled social-icon foot-social-icon text-sm-end mb-0">
                            {#each social as item }
                            <li class="list-inline-item me-1"><Link to={item.link}
                                    target="_blank" class="rounded"><i data-feather={item.icon}
                                        class="fea icon-sm align-middle" title="dribbble"></i></Link></li>
                                
                            {/each}
                        </ul><!--end icon-->
                    </div><!--end col-->
                </div><!--end row-->
            </div><!--end container-->
        </div>
    </footer><!--end footer-->
    <!-- Footer End -->
</main>


<style lang="scss" scoped></style>