<script>
    import image from '../../assets/images/company/facebook-logo.png'
    import image2 from '../../assets/images/company/google-logo.png'
    import image3 from '../../assets/images/company/android.png'
    import image4 from '../../assets/images/company/lenovo-logo.png'
    import image5 from '../../assets/images/company/spotify.png'
    import image6 from '../../assets/images/company/linkedin.png'
    import image7 from '../../assets/images/company/circle-logo.png';
    import image8 from '../../assets/images/company/skype.png';
    import image9 from '../../assets/images/company/snapchat.png';
    import image10 from '../../assets/images/company/shree-logo.png';
    import image11 from '../../assets/images/company/telegram.png';
    import image12 from '../../assets/images/company/whatsapp.png';
    import { Link } from 'svelte-routing'
    
    const JobData = [
        {
            id: 1,
            image: image,
            name: 'Facebook',
            time: '2 days ago',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
        },
        {
            id: 2,
            image: image2,
            name: 'Google',
            time: '2 days ago',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
        },
        {
            id: 3,
            image: image3,
            name: 'Android',
            time: '2 days ago',
            type: 'Remote',
            title: 'Application Developer',
            city: 'Australia',
        },
        {
            id: 4,
            image: image4,
            name: 'Lenovo',
            time: '2 days ago',
            type: 'WFH',
            title: 'Senior Product Designer',
            city: 'Australia',
        },
        {
            id: 5,
            image: image5,
            name: 'Spotify',
            time: '2 days ago',
            type: 'Full Time',
            title: 'C++ Developer',
            city: 'Australia',
        },
        {
            id: 6,
            image: image6,
            name: 'Linkedin',
            time: '2 days ago',
            type: 'Remote',
            title: 'Php Developer',
            city: 'Australia',
        },
        {
            id: 7,
            image: image7,
            name: 'Circle CI',
            time: '2 days ago',
            type: 'Full Time',
            title: 'Web Designer / Developer',
            city: 'Australia',
        },
        {
            id: 8,
            image: image8,
            name: 'Skype',
            time: '2 days ago',
            type: 'Part Time',
            title: 'Marketing Director',
            city: 'Australia',
        },
        {
            id: 9,
            image: image9,
            name: 'Snapchat',
            time: '2 days ago',
            type: 'Remote',
            title: 'Application Developer',
            city: 'Australia',
        },
        {
            id: 10,
            image: image10,
            name: 'Shreethemes',
            time: '2 days ago',
            type: 'WFH',
            title: 'Senior Product Designer',
            city: 'Australia',
        },
        {
            id: 11,
            image: image11,
            name: 'Telegram',
            time: '2 days ago',
            type: 'Full Time',
            title: 'C++ Developer',
            city: 'Australia',
        },
        {
            id: 12,
            image: image12,
            name: 'Whatsapp',
            time: '2 days ago',
            type: 'Remote',
            title: 'Php Developer',
            city: 'Australia',
        }
    ]
    
    </script>

<main>
    <div class="row g-4">
        {#each JobData as item}
        <div class="col-lg-4 col-md-6 col-12">
            <div class="job-post rounded shadow p-4">
                <div class="d-flex align-items-center justify-content-between">
                    <div class="d-flex align-items-center">
                        <img src={item.image} class="avatar avatar-small rounded shadow p-3 bg-white" alt="">

                        <div class="ms-3">
                            <Link to={`/employer-profile/${item.id}`} class="h5 company text-dark">{ item.name
                                }</Link>
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