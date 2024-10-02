<script>
    import image from '../assets/images/team/04.jpg';
    import image2 from '../assets/images/team/05.jpg';
    import image3 from '../assets/images/team/06.jpg';
    import image4 from '../assets/images/team/07.jpg';
    import { Link } from 'svelte-routing';
    
    const datas = [
        {
            image: image,
            social: ['facebook', 'instagram', 'twitter'],
            name: 'Jack John',
            position: 'Job Seeker'
        },
        {
            image: image2,
            social: ['facebook', 'instagram', 'twitter'],
            name: 'Krista John',
            position: 'Job Seeker'
        },
        {
            image: image3,
            social: ['facebook', 'instagram', 'twitter'],
            name: 'Roger Jackson',
            position: 'Job Seeker'
        },
        {
            image: image4,
            social: ['facebook', 'instagram', 'twitter'],
            name: 'Johnny English',
            position: 'Job Seeker'
        },
    ]
    
    </script>

<main>
    <div class="row justify-content-center">
        <div class="col">
            <div class="section-title text-center mb-4 pb-2">
                <h4 class="title mb-3">Our Minds</h4>
                <p class="text-muted para-desc mb-0 mx-auto">Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row g-4 mt-0">
        {#each datas as item }
        <div class="col-lg-3 col-md-4 col-12">
            <div class="card team team-primary text-center">
                <div
                    class="card-img team-image d-inline-block mx-auto rounded-pill avatar avatar-ex-large overflow-hidden">
                    <img src={item.image} class="img-fluid" alt="">
                    <div class="card-overlay avatar avatar-ex-large rounded-pill"></div>

                    <ul class="list-unstyled team-social mb-0">
                        {#each item.social as social}
                        <li  class="list-inline-item me-1"><a
                                href="#name" class="btn btn-sm btn-pills btn-icon"><i
                                    data-feather={social} class="icons fea-social"></i></a></li>
                                    {/each}
                    </ul><!--end icon-->
                </div>

                <div class="content mt-3">
                    <Link to="/page-team-detail" class="text-dark h5 mb-0 title">{ item.name }</Link>
                    <h6 class="text-muted mb-0 fw-normal">{ item.position }</h6>
                </div>
            </div>
        </div><!--end col-->
        {/each}
       

    </div><!--end row-->
</main>

<style lang="scss" scoped></style>