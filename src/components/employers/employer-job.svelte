<script>
  import { Link } from 'svelte-routing';
  import Pagination from '../../components/pagination.svelte';
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
  
  const employers = [
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
    {
      id: 5,
      image: image5,
      name: 'Spotify',
      city: 'Australia',
      jobs: 6,
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 6,
      image: image6,
      name: 'Linkedin',
      city: 'Australia',
      jobs: 6,
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 7,
      image: image7,
      name: 'Circle CI',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 8,
      image: image8,
      name: 'Skype',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 9,
      image: image9,
      name: 'Snapchat',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 10,
      image: image10,
      name: 'Shreethemes',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 11,
      image: image11,
      name: 'Telegram',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    },
    {
      id: 12,
      image: image12,
      name: 'Whatsapp',
      city: 'Australia',
      desctwo: 'Digital Marketing Solutions for Tomorrow'
    }]
  </script>

<main>
  <div class="container">
    <div class="row g-4 gy-5">
      {#each employers as employer}
      <div class="col-lg-3 col-md-4 col-sm-6 col-12">
        <div class="employer-card position-relative bg-white rounded shadow p-4 mt-3">
          <div class="employer-img d-flex justify-content-center align-items-center bg-white shadow-md rounded">
            <img src={employer.image} class="avatar avatar-ex-small" alt="">
          </div>

          <div class="content mt-3">
            <Link to={`/employer-profile/${employer.id}`} class="title text-dark h5">{
              employer.name }</Link>

            <p class="text-muted mt-2 mb-0">{ employer.desctwo }</p>
          </div>

          <ul class="list-unstyled d-flex justify-content-between align-items-center border-top mt-3 pt-3 mb-0">
            <li class="text-muted d-inline-flex align-items-center">
              <i data-feather="map-pin" class="fea icon-sm me-1 align-middle"></i>
              { employer.city }
            </li>
            <li class="list-inline-item text-primary fw-medium">{ employer.jobs } Jobs</li>
          </ul>
        </div>
      </div>
      {/each}
      
    </div>

    <Pagination />
  </div><!--end container-->
</main>

<style lang="scss" scoped></style>