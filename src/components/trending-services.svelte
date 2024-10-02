<script>
    import { onMount } from 'svelte';
    import { tns } from 'tiny-slider/src/tiny-slider';
    import image from '../assets/images/work/01.jpg';
    import image2 from '../assets/images/work/02.jpg';
    import image3 from '../assets/images/work/03.jpg';
    import image4 from '../assets/images/work/04.jpg';
    import image5 from '../assets/images/work/05.jpg';
    import image6 from '../assets/images/work/06.jpg';
    
    const datas = [
        {
            image: image,
            name: 'Product & Branding Design'
        },
        {
            image: image2,
            name: 'Wordpress Development'
        },
        {
            image: image3,
            name: 'Audio & Video Editing'
        },
        {
            image: image4,
            name: 'Admin & Customer Support'
        },
        {
            image: image5,
            name: 'UX / UI Designer'
        },
        {
            image: image6,
            name: 'Digital Marketing'
        },
    ]
    
    onMount(() => {
        tns({
            container: '.tiny-five-item',
            controls: true,
            mouseDrag: true,
            loop: true,
            rewind: true,
            autoplay: true,
            autoplayButtonOutput: false,
            autoplayTimeout: 3000,
            navPosition: "bottom",
            controlsText: ['<i class="mdi mdi-chevron-left "></i>', '<i class="mdi mdi-chevron-right"></i>'],
            nav: false,
            speed: 400,
            gutter: 0,
            responsive: {
                1025: {
                    items: 5
                },
    
                992: {
                    items: 4
                },
    
                767: {
                    items: 3
                },
    
                425: {
                    items: 1
                },
            },
        });
    });
    
    </script>

<main>
    <div class="container">
        <div class="row justify-content-center mb-4 pb-2">
            <div class="col-12">
                <div class="section-title text-center">
                    <h4 class="title mb-3">Trending Services</h4>
                    <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
                        personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
                </div>
            </div><!--end col-->
        </div><!--end row-->

        <div class="row">
            <div class="col-12 mt-4">
                <div class="tiny-five-item">
                    {#each datas as item }
                    <div class="tiny-slide">
                        <div class="card features rounded shadow position-relative overflow-hidden m-2">
                            <div class="card-body p-0">
                                <div class="card-img">
                                    <img src={item.image} class="img-fluid" alt="">
                                    <div class="card-overlay"></div>
                                </div>

                                <div class="position-absolute bottom-0 start-0 m-3">
                                    <a href="#name" class="title h5 text-white">{ item.name }</a>
                                </div>
                            </div>
                        </div>
                    </div><!--end col-->
                    {/each}
                   
                </div>
            </div>
        </div>
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>