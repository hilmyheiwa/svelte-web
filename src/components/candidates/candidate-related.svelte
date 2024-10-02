<script>
    import image from '../../assets/images/team/02.jpg';
    import image2 from '../../assets/images/team/03.jpg';
    import image3 from '../../assets/images/team/04.jpg';
    import image4 from '../../assets/images/team/05.jpg';
    import { Link } from 'svelte-routing';
    
    const candidates = [
        {
            id: 2,
            image: image,
            name: 'Tiffany Betancourt',
            jobTitle: 'Application Developer',
            skills: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
        },
        {
            id: 3,
            image: image2,
            name: 'Jacqueline Burns',
            jobTitle: 'Senior Product Designer',
            skills: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
        },
        {
            id: 4,
            image: image3,
            name: 'Mari Harrington',
            jobTitle: 'C++ Developer',
            skills: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
        },
        {
            id: 5,
            image: image4,
            name: 'Floyd Glasgow',
            jobTitle: 'Php Developer',
            skills: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
        }
    ]
    
    </script>

<main>
    <div>
        <!-- Section title -->
        <div class="row justify-content-center mb-4 pb-2">
            <div class="col-12">
                <div class="section-title text-center">
                    <h4 class="title mb-3">Related Candidates</h4>
                    <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
                        personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
                </div>
            </div><!--end col-->
        </div><!--end row-->

        <!-- Candidate cards -->
        <div class="row">
            {#each candidates as candidate, index}
            <div 
            class="col-lg-3 col-md-4 col-sm-6 col-12 mt-4 pt-2">
            <div class="candidate-card position-relative overflow-hidden text-center shadow rounded p-4">
                <div class="content">
                    {#if index===2 }
                    <div class="ribbon ribbon-left overflow-hidden"><span
                        class="text-center d-block bg-warning shadow small h6"><i
                            class="mdi mdi-star"></i></span></div>
                    {/if}
                   
                    <img src={candidate.image} class="avatar avatar-md-md rounded-pill shadow-md" alt="">

                    <div class="mt-3">
                        <Link to={`/candidate-profile/${candidate.id}`} class="title h5 text-dark">{
                            candidate.name
                            }</Link>
                        <p class="text-muted mt-1">{ candidate.jobTitle }</p>

                        {#each candidate.skills as skill }
                        <span 
                        class="badge bg-soft-primary rounded-pill me-1">{ skill }</span>
                        {/each}
                       
                    </div>

                    <div class="mt-2 d-flex align-items-center justify-content-between">
                        <div class="text-center">
                            <p class="text-muted fw-medium mb-0">Salary:</p>
                            <p class="mb-0 fw-medium">{ candidate.salary }</p>
                        </div>

                        <div class="text-center">
                            <p class="text-muted fw-medium mb-0">Experience:</p>
                            <p class="mb-0 fw-medium">{ candidate.experience }</p>
                        </div>
                    </div>

                    <div class="mt-3">
                        <Link to={`/candidate-profile/${candidate.id}`}
                            class="btn btn-sm btn-primary me-1">View
                            Profile</Link>
                        <Link to="/contactus" class="btn btn-sm btn-icon btn-soft-primary"><i
                                data-feather="message-circle" class="icons"></i></Link>
                    </div>

                    <a href="#name" class="like"><i class="mdi mdi-heart align-middle fs-4"></i></a>
                </div>
            </div>
        </div><!--end col-->
            {/each}
           
        </div><!--end row-->
    </div>
</main>

<style lang="scss" scoped>
/* Add your styles here */
</style>