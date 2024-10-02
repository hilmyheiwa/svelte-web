<script>
  import Sidebar from '../../components/job-sidebar.svelte'
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
  import Pagination from '../../components/pagination.svelte'
  
  const jobData = [
    {
      id: 1,
      image: image,
      name: 'Facebook',
      time: 'Posted 3 Days ago',
      type: 'Full Time',
      title: 'Web Designer / Developer',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 2,
      image: image2,
      name: 'Google',
      time: 'Posted 3 Days ago',
      type: 'Part Time',
      title: 'Marketing Director',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 3,
      image: image3,
      name: 'Android',
      time: 'Posted 3 Days ago',
      type: 'Remote',
      title: 'Application Developer',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 4,
      image: image4,
      name: 'Lenovo',
      time: 'Posted 3 Days ago',
      type: 'WFH',
      title: 'Senior Product Designer',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 5,
      image: image5,
      name: 'Spotify',
      time: 'Posted 3 Days ago',
      type: 'Full Time',
      title: 'C++ Developer',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 6,
      image: image6,
      name: 'Linkedin',
      time: 'Posted 3 Days ago',
      type: 'Remote',
      title: 'Php Developer',
      city: 'Australia',
      salary: '$950 - $1100/mo',
    },
    {
      id: 7,
      image: image7,
      name: 'Circle CI',
      type: 'Full Time',
      title: 'Web Designer / Developer',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    },
    {
      id: 8,
      image: image8,
      name: 'Skype',
      type: 'Part Time',
      title: 'Marketing Director',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    },
    {
      id: 9,
      image: image9,
      name: 'Snapchat',
      type: 'Remote',
      title: 'Application Developer',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    },
    {
      id: 10,
      image: image10,
      name: 'Shreethemes',
      type: 'WFH',
      title: 'Senior Product Designer',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    },
    {
      id: 11,
      image: image11,
      name: 'Telegram',
      type: 'Full Time',
      title: 'C++ Developer',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    },
    {
      id: 12,
      image: image12,
      name: 'Whatsapp',
      type: 'Remote',
      title: 'Php Developer',
      city: 'Australia',
      time: 'Posted 3 Days ago',
      salary: '$950 - $1100/mo',
    }
  ]
  </script>

<main>
    <div class="container">
        <div class="row g-4">
            <Sidebar />

            <div class="col-lg-8 col-md-6 col-12">
                <div class="row g-4">
                  {#each jobData as item}
                  <div class="col-lg-6 col-12">
                    <div class="job-post rounded shadow bg-white">
                        <div class="p-4">
                            <Link to={`/job-detail-two/${item.id}`}
                                class="text-dark title h5">{ item.title
                                }</Link>

                            <p class="text-muted d-flex align-items-center small mt-3"><i data-feather="clock"
                                    class="fea icon-sm text-primary me-1"></i>{ item.time }
                            </p>

                            <ul class="list-unstyled d-flex justify-content-between align-items-center mb-0 mt-3">
                                <li class="list-inline-item"><span class="badge bg-soft-primary">{ item.type
                                        }</span>
                                </li>
                                <li class="list-inline-item"><span
                                        class="text-muted d-flex align-items-center small"><i
                                            data-feather="dollar-sign" class="fea icon-sm text-primary me-1"></i>{
                                                item.salary }</span></li>
                            </ul>
                        </div>
                        <div class="d-flex align-items-center p-4 border-top">
                            <img src={item.image}
                                class="avatar avatar-small rounded shadow p-3 bg-white" alt="">

                            <div class="ms-3">
                                <Link to={`/employer-profile/${item.id}`}
                                    class="h5 company text-dark">{ item.name
                                    }</Link>
                                <span class="text-muted d-flex align-items-center mt-1"><i data-feather="map-pin"
                                        class="fea icon-sm me-1"></i>{ item.city }</span>
                            </div>
                        </div>
                    </div>
                </div><!--end col-->
                  {/each}

                </div><!--end row-->

                <Pagination />
            </div>
        </div>
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>