<script>
    import { Link } from 'svelte-routing';
    import image from '../../assets/images/company/facebook-logo.png';
    import image2 from '../../assets/images/company/google-logo.png';
    import image3 from '../../assets/images/company/android.png';
    
    const jobData = [
        {
            id: 1,
            image: image,
            name: 'Facebook',
            time: '2 days ago',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 2,
            image: image2,
            name: 'Google',
            time: '2 days ago',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 3,
            image: image3,
            name: 'Android',
            time: '2 days ago',
            type: 'Remote',
            title: 'Application Developer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
    ]
    
    </script>

<main>
    <div class="row justify-content-center mb-4 pb-2">
        <div class="col-12">
            <div class="section-title text-center">
                <h4 class="title mb-3">Related Vacancies</h4>
                <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row">
        {#each jobData as item}
        <div class="col-lg-4 col-md-6 col-12 mt-4 pt-2">
            <div class="job-post rounded shadow p-4">
                <div class="d-flex align-items-center justify-content-between">
                    <div class="d-flex align-items-center">
                        <img src={item.image}
                            class="avatar avatar-small rounded shadow p-3 bg-white" alt="">

                        <div class="ms-3">
                            <Link to={`/employer-profile/${item.job}`} class="h5 company text-dark">{ item.name }
                            </Link>
                            <span class="text-muted d-flex align-items-center small mt-2"><i data-feather="clock"
                                    class="fea icon-sm me-1"></i> { item.time }</span>
                        </div>
                    </div>

                    <span class="badge bg-soft-primary">{ item.type }</span>
                </div>

                <div class="mt-4">
                    <Link to={`/job-detail-one/${item.id}`} class="text-dark title h5">{
                        item.title }</Link>

                    <span class="text-muted d-flex align-items-center mt-2"><i data-feather="map-pin"
                            class="fea icon-sm me-1"></i>{ item.city }</span>

                    <div class="progress-box mt-3">
                        <div class="progress mb-2">
                            <div class="progress-bar position-relative bg-primary" style="width:50%;"></div>
                        </div>

                        <span class="text-dark">20 applied of <span class="text-muted">40 vacancy</span></span>
                    </div>
                </div>
            </div><!--end job post-->
        </div><!--end col-->
        {/each}
        
    </div><!--end row-->
</main>

<style lang="scss" scoped></style>