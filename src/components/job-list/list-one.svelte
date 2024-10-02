<script>
    import { Link } from 'svelte-routing';
    import image from '../../assets/images/company/facebook-logo.png';
    import image2 from '../../assets/images/company/google-logo.png';
    import image3 from '../../assets/images/company/android.png';
    import image4 from '../../assets/images/company/lenovo-logo.png';
    import image5 from '../../assets/images/company/spotify.png';
    import image6 from '../../assets/images/company/linkedin.png';
    import image7 from '../../assets/images/company/circle-logo.png';
    import image8 from '../../assets/images/company/skype.png';
    
    
  export let width;
    
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
        {
            id: 4,
            image: image4,
            name: 'Lenovo',
            time: '2 days ago',
            type: 'WFH',
            title: 'Senior Product Designer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 5,
            image: image5,
            name: 'Spotify',
            time: '2 days ago',
            type: 'Full Time',
            title: 'C++ Developer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 6,
            image: image6,
            name: 'Linkedin',
            time: '2 days ago',
            type: 'Remote',
            title: 'Php Developer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 7,
            image: image7,
            name: 'Circle CI',
            time: '2 days ago',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
        {
            id: 8,
            image: image8,
            name: 'Skype',
            time: '2 days ago',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
            salary: '$950 - $1100/mo',
        },
    ]
</script>

<div class="row g-4">
    {#each jobData as item}
    <div  class="col-12">
        <div
            class="job-post job-post-list rounded shadow p-4 d-md-flex align-items-center justify-content-between position-relative"
        >
            <div class={`d-flex align-items-center ${width}`}>
                <img
                    src={item.image}
                    class="avatar avatar-small rounded shadow p-3 bg-white"
                    alt=""
                />

                <div class="ms-3">
                    <Link
                        to={`/job-detail-one/${item.id}`}
                        class="h5 title text-dark"
                        >{item.title}
                    </Link>
                </div>
            </div>

            <div
                class="d-flex align-items-center justify-content-between d-md-block mt-3 mt-md-0 w-100px"
            >
                <span class="badge bg-soft-primary rounded-pill"
                    >{item.type}</span
                >
                <span
                    class="text-muted d-flex align-items-center fw-medium mt-md-2"
                    ><i
                        data-feather="clock"
                        class="fea icon-sm me-1 align-middle"
                    ></i>{item.time}</span
                >
            </div>

            <div
                class="d-flex align-items-center justify-content-between d-md-block mt-2 mt-md-0 w-130px"
            >
                <span class="text-muted d-flex align-items-center"
                    ><i
                        data-feather="map-pin"
                        class="fea icon-sm me-1 align-middle"
                    ></i>{item.city}</span
                >
                <span class="d-flex fw-medium mt-md-2">{item.salary}</span>
            </div>

            <div class="mt-3 mt-md-0">
                <a
                    href="#name"
                    class="btn btn-sm btn-icon btn-pills btn-soft-primary bookmark"
                    ><i data-feather="bookmark" class="icons"></i></a
                >
                <Link
                    to={`/job-detail-one/${item.id}`}
                    class="btn btn-sm btn-primary w-full ms-md-1"
                    >Apply Now
                </Link>
            </div>
        </div>
    </div>
    {/each}
   
    <!--end col-->
</div>

<!--end row-->

<style lang="scss" scoped></style>
