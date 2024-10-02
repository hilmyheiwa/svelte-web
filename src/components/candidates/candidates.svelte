<script>
    import image from '../../assets/images/team/01.jpg';
    import image2 from '../../assets/images/team/02.jpg';
    import image3 from '../../assets/images/team/03.jpg';
    import image4 from '../../assets/images/team/04.jpg';
    import image5 from '../../assets/images/team/05.jpg';
    import image6 from '../../assets/images/team/06.jpg';
    import image7 from '../../assets/images/team/07.jpg';
    import image8 from '../../assets/images/team/08.jpg';
    import image9 from '../../assets/images/team/01.jpg';
    import image10 from '../../assets/images/team/02.jpg';
    import image11 from '../../assets/images/team/03.jpg';
    import image12 from '../../assets/images/team/04.jpg';
    import Pagination from '../../components/pagination.svelte';
    import { Link } from 'svelte-routing';
    
    const datas = [
        {
            id: 1,
            image: image,
            name: 'Steven Townsend',
            position: 'Marketing Director',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: true,
        },
        {
            id: 2,
            image: image2,
            name: 'Tiffany Betancourt',
            position: 'Application Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 3,
            image: image3,
            name: 'Jacqueline Burns',
            position: 'Senior Product Designer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 4,
            image: image4,
            name: 'Mari Harrington',
            position: 'C++ Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: true,
        },
        {
            id: 5,
            image: image5,
            name: 'Floyd Glasgow',
            position: 'Php Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 6,
            image: image6,
            name: 'Donna Schultz',
            position: 'Web Designer / Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 7,
            image: image7,
            name: 'Joshua Morris',
            position: 'Marketing Director',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 8,
            image: image8,
            name: 'Rosaria Vargas',
            position: 'Application Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: true,
        },
        {
            id: 9,
            image: image9,
            name: 'Steven Townsend',
            position: 'Marketing Director',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
        {
            id: 10,
            image: image10,
            name: 'Tiffany Betancourt',
            position: 'Application Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: true,
        },
        {
            id: 11,
            image: image11,
            name: 'Jacqueline Burns',
            position: 'Senior Product Designer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: true,
        },
        {
            id: 12,
            image: image12,
            name: 'Mari Harrington',
            position: 'C++ Developer',
            languages: ['Design', 'UI', 'UX', 'Digital'],
            salary: '$5k - $6k',
            experience: '2 Years',
            show: false,
        },
    ]
    
    </script>

<main>
    <div class="container">
        <div class="row g-4">
            {#each datas as item}
            <div class="col-lg-3 col-md-4 col-sm-6 col-12">
                <div class="candidate-card position-relative overflow-hidden text-center shadow rounded p-4">
                    {#if item.show=== true}
                    <div class="ribbon ribbon-left overflow-hidden"><span
                            class="text-center d-block bg-warning shadow small h6"><i class="mdi mdi-star"></i></span>
                    </div>
                    {/if}
                    <div class="content">
                        <img src={item.image} class="avatar avatar-md-md rounded-pill shadow-md" alt="">

                        <div class="mt-3">
                            <Link to={`/candidate-profile/${item.id}`} class="title h5 text-dark">{ item.name }
                            </Link>
                            <p class="text-muted mt-1">{ item.position }</p>
                              
                            {#each item.languages as language }
                            <span 
                                class="badge bg-soft-primary rounded-pill me-1">{ language }</span>                                
                            {/each}

                        </div>

                        <div class="mt-2 d-flex align-items-center justify-content-between">
                            <div class="text-center">
                                <p class="text-muted fw-medium mb-0">Salary:</p>
                                <p class="mb-0 fw-medium">{ item.salary }</p>
                            </div>

                            <div class="text-center">
                                <p class="text-muted fw-medium mb-0">Experience:</p>
                                <p class="mb-0 fw-medium">{ item.experience }</p>
                            </div>
                        </div>

                        <div class="mt-3">
                            <Link to={`/candidate-profile/${item.id}`} class="btn btn-sm btn-primary me-1">View
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

        <Pagination />
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>