<script>
    import image from '../../assets/images/company/facebook-logo.png';
    import image2 from '../../assets/images/company/google-logo.png';
    import image3 from '../../assets/images/company/android.png';
    import image4 from '../../assets/images/company/lenovo-logo.png';
    import { Link } from 'svelte-routing';
    
    const jobData = [
        {
            id: 1,
            image: image,
            name: 'Facebook',
            city: 'Australia',
            jobs: 6,
            desctwo: 'Digital Marketing Solutions for Tomorrow'
        },
        {
            id: 2,
            image: image2,
            name: 'Google',
            city: 'Australia',
            jobs: 6,
            desctwo: 'Digital Marketing Solutions for Tomorrow'
        },
        {
            id: 3,
            image: image3,
            name: 'Android',
            city: 'Australia',
            jobs: 6,
            desctwo: 'Digital Marketing Solutions for Tomorrow'
        },
        {
            id: 4,
            image: image4,
            name: 'Lenovo',
            city: 'Australia',
            jobs: 6,
            desctwo: 'Digital Marketing Solutions for Tomorrow'
        },
    ]
    
    </script>

<main>
    <div class="row justify-content-center mb-4 pb-2">
        <div class="col-12">
            <div class="section-title text-center">
                <h4 class="title mb-3">Related Companies</h4>
                <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row">
        {#each jobData as item }
        <div class="col-lg-3 col-md-4 col-sm-6 col-12 mt-5">
            <div class="employer-card position-relative bg-white rounded shadow p-4 mt-3">
                <div class="employer-img d-flex justify-content-center align-items-center bg-white shadow-md rounded">
                    <img src={item.image} class="avatar avatar-ex-small" alt="">
                </div>

                <div class="content mt-3">
                    <Link to={`/employer-profile/${item.id}`} class="title text-dark h5">{item.name}</Link>

                    <p class="text-muted mt-2 mb-0">{ item.desctwo }</p>
                </div>

                <ul class="list-unstyled d-flex justify-content-between align-items-center border-top mt-3 pt-3 mb-0">
                    <li class="text-muted d-inline-flex align-items-center"><i data-feather="map-pin"
                            class="fea icon-sm me-1 align-middle"></i>{ item.city }</li>
                    <li class="list-inline-item text-primary fw-medium">{ item.jobs } jobs</li>
                </ul>
            </div>
        </div><!--end col-->
        {/each}
       
    </div><!--end row-->
</main>

<style lang="scss" scoped></style>