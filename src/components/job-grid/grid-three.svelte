<script setup>
    import image from '../../assets/images/company/facebook-logo.png';
    import image2 from '../../assets/images/company/google-logo.png';
    import image3 from '../../assets/images/company/android.png';
    import image4 from '../../assets/images/company/lenovo-logo.png';
    import image5 from '../../assets/images/company/spotify.png';
    import image6 from '../../assets/images/company/linkedin.png';
    import image7 from '../../assets/images/company/circle-logo.png';
    import image8 from '../../assets/images/company/skype.png';
    import image9 from '../../assets/images/company/snapchat.png';
    import image10 from '../../assets/images/company/shree-logo.png';
    import image11 from '../../assets/images/company/telegram.png';
    import image12 from '../../assets/images/company/whatsapp.png';
    import { Link } from 'svelte-routing';
    
    const JobData = [
        {
            id: 1,
            image: image,
            name: 'Facebook',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 2,
            image: image2,
            name: 'Google',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 3,
            image: image3,
            name: 'Android',
            type: 'Remote',
            title: 'Application Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 4,
            image: image4,
            name: 'Lenovo',
            type: 'WFH',
            title: 'Senior Product Designer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 5,
            image: image5,
            name: 'Spotify',
            type: 'Full Time',
            title: 'C++ Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 6,
            image: image6,
            name: 'Linkedin',
            type: 'Remote',
            title: 'Php Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 7,
            image: image7,
            name: 'Circle CI',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 8,
            image: image8,
            name: 'Skype',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 9,
            image: image9,
            name: 'Snapchat',
            type: 'Remote',
            title: 'Application Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 10,
            image: image10,
            name: 'Shreethemes',
            type: 'WFH',
            title: 'Senior Product Designer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 11,
            image: image11,
            name: 'Telegram',
            type: 'Full Time',
            title: 'C++ Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        },
        {
            id: 12,
            image: image12,
            name: 'Whatsapp',
            type: 'Remote',
            title: 'Php Developer',
            city: 'Australia',
            desc: 'Looking for an experienced Web Designer for an our company.',
            salarytwo: '$4,000 - $4,500',
        }
    ]
    </script>

<main>
    <div class="row g-4">
        {#each JobData as item}
        <div class="col-lg-4 col-md-6 col-12">
            <div class="job-post job-type-three rounded shadow bg-white p-4">
                <div class="d-flex justify-content-between">
                    <div>
                        <img src={item.image} class="avatar avatar-small rounded shadow p-3 bg-white" alt="">
                        <Link to={`/employer-profile/${item.id}`} class="h5 company text-dark d-block mt-2">{
                            item.name }</Link>
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
                    <Link to={`/job-detail-three/${item.id}`} class="text-dark title h5">{
                        item.title }</Link>
                    <p class="text-muted mt-2">{ item.desc }</p>

                    <ul class="list-unstyled mb-0">
                        <li class="d-inline-block me-1"><a href="#type" class="badge bg-primary">{ item.type }</a></li>
                        <li class="d-inline-block me-1"><a href="#salary" class="badge bg-primary">{ item.salarytwo }</a>
                        </li>
                        <li class="d-inline-block me-1"><a href="#city" class="badge bg-primary"><i
                                    class="mdi mdi-map-marker me-1"></i>{ item.city }</a></li>
                    </ul>
                </div>
            </div>
        </div><!--end col-->
        {/each}
       
    </div><!--end row-->
</main>

<style lang="scss" scoped></style>