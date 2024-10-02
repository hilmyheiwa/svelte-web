<script>
  import { Link } from 'svelte-routing';
  import image from '../assets/images/company/facebook-logo.png';
  import image2 from '../assets/images/company/google-logo.png';
  import image3 from '../assets/images/company/android.png';
  import image4 from '../assets/images/company/lenovo-logo.png';
  import image5 from '../assets/images/company/spotify.png';
  import image6 from '../assets/images/company/linkedin.png';
  
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
  ]
  
  </script>

<main>
  <div>
    <div class="row justify-content-center mb-4 pb-2">
      <div class="col-12">
        <div class="section-title text-center">
          <h4 class="title mb-3">Popular Job Listing</h4>
          <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
            personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
        </div>
      </div><!--end col-->
    </div><!--end row-->

    <div class="row g-4 mt-0">
      {#each jobData as job}
      <div class="col-lg-4 col-md-6 col-12">
        <div class="job-post rounded shadow bg-white">
          <div class="p-4">
            <Link to={`/job-detail-two/${job.id}`} class="text-dark title h5">{ job.title }</Link>

            <p class="text-muted d-flex align-items-center small mt-3"><i data-feather="clock"
                class="fea icon-sm text-primary me-1"></i> { job.time } </p>

            <ul class="list-unstyled d-flex justify-content-between align-items-center mb-0 mt-3">
              <li class="list-inline-item"><span class="badge bg-soft-primary">{ job.type }</span></li>
              <li class="list-inline-item"><span class="text-muted d-flex align-items-center small"><i
                    data-feather="dollar-sign" class="fea icon-sm text-primary me-1"></i>{ job.salary }</span></li>
            </ul>
          </div>
          <div class="d-flex align-items-center p-4 border-top">
            <img src={job.image} class="avatar avatar-small rounded shadow p-3 bg-white" alt="">

            <div class="ms-3">
              <Link to={`/job-detail-two/${job.id}`} class="h5 company text-dark">{ job.name }</Link>
              <span class="text-muted d-flex align-items-center mt-1"><i data-feather="map-pin"
                  class="fea icon-sm me-1"></i>{ job.city }</span>
            </div>
          </div>
        </div>
      </div><!--end col-->
      {/each}
      
    </div><!--end row-->
  </div>
</main>
