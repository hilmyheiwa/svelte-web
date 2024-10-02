<script>
    import { Link } from 'svelte-routing';
    import image from '../../assets/images/company/google-logo.png';
    import image2 from '../../assets/images/company/android.png';
    import image3 from '../../assets/images/company/lenovo-logo.png';
    
    const jobs = [
        {
            companyLogo: image,
            companyName: 'Google',
            jobTitle: 'Marketing Director',
            jobDescription: 'Looking for an experienced Web Designer for an our company.',
            badges: [
                { text: 'Part Time' },
                { text: '$4,000 - $4,500', },
                { text: 'Australia', icon: 'mdi mdi-map-marker' }
            ]
        },
        {
            companyLogo: image2,
            companyName: 'Android',
            jobTitle: 'Application Developer',
            jobDescription: 'Looking for an experienced Web Designer for an our company.',
            badges: [
                { text: 'Remote' },
                { text: '$4,000 - $4,500', },
                { text: 'Australia', icon: 'mdi mdi-map-marker' }
            ]
        },
        {
            companyLogo: image3,
            companyName: 'Lenovo',
            jobTitle: 'Senior Product Designer',
            jobDescription: 'Looking for an experienced Web Designer for an our company.',
            badges: [
                { text: 'WFH' },
                { text: '$4,000 - $4,500', },
                { text: 'Australia', icon: 'mdi mdi-map-marker' }]
        }
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
        {#each jobs as job }
        <div class="col-lg-4 col-md-6 col-12 mt-4 pt-2">
            <div class="job-post job-type-three rounded shadow bg-white p-4">
                <div class="d-flex justify-content-between">
                    <div>
                        <img src={job.companyLogo} class="avatar avatar-small rounded shadow p-3 bg-white" alt="">
                        <Link to="/employer-profile" class="h5 company text-dark d-block mt-2">{ job.companyName
                            }</Link>
                    </div>

                    <ul class="list-unstyled align-items-center mb-0">
                        <li class="list-inline-item"><a href="#name" class="like me-1"><i
                                    class="mdi mdi-heart align-middle fs-3"></i></a></li>
                        <li class="list-inline-item"><a href="#name" class="btn btn-icon btn-sm btn-soft-primary me-1"><i
                                    data-feather="bookmark" class="icons"></i></a></li>
                        <li class="list-inline-item"><a href="#name" class="btn btn-icon btn-sm btn-soft-primary"><i
                                    data-feather="arrow-up-right" class="icons"></i></a></li>
                    </ul>
                </div>

                <div class="mt-2">
                    <Link to="/job-detail-three" class="text-dark title h5">{ job.jobTitle }</Link>
                    <p class="text-muted mt-2">{ job.jobDescription }</p>

                    <ul class="list-unstyled mb-0">
                        {#each job.badges as badge }
                        <li class="d-inline-block me-1">
                            <Link to="#" class="badge bg-primary">{ badge.text }<i 
                                    class={badge.icon}></i></Link>
                        </li>
                        {/each}
                    </ul>
                </div>
            </div>
        </div>
        {/each}
        
    </div>
</main>

<style lang="scss" scoped></style>