<script>
import { Link } from "svelte-routing";

  const jobCategories = [
    {
      title: 'Business',
      titletwo: 'Development',
      count: '74',
      icon: 'airplay'
    },
    {
      title: 'Marketing &',
      titletwo: 'Communication',
      count: '20',
      icon: 'award'
    },
    {
      title: 'Project',
      titletwo: 'Management',
      count: '35',
      icon: 'at-sign'
    },
    {
      title: 'Customer',
      titletwo: 'Service',
      count: '46',
      icon: 'codesandbox'
    },
    {
      title: 'Software',
      titletwo: 'Engineering',
      count: '60',
      icon: 'chrome'
    },
    {
      title: 'Human Resource',
      titletwo: 'HR',
      count: '74',
      icon: 'copy'
    },
    {
      title: 'It &',
      titletwo: 'Networking',
      count: '20',
      icon: 'cpu'
    },
    {
      title: 'Sales &',
      titletwo: 'Marketing',
      count: '35',
      icon: 'inbox'
    },
    {
      title: 'Project',
      titletwo: 'Manager',
      count: '46',
      icon: 'thumbs-up'
    },
    {
      title: 'Data',
      titletwo: 'Science',
      count: '60',
      icon: 'umbrella'
    }
  ];
  </script>

<main>
  <div class="container">
    <div class="row row-cols-lg-5 row-col-md-4 row-cols-sm-2 row-cols-1 g-4">
      {#each jobCategories as job}
      <div class="col">
        <div class="position-relative job-category text-center px-4 py-5 rounded shadow">
          <div
            class="feature-icon bg-soft-primary rounded shadow mx-auto position-relative overflow-hidden d-flex justify-content-center align-items-center">
            <i data-feather={job.icon} class="fea icon-ex-md"></i>
          </div>

          <div class="mt-4">
            <Link to="#" class="title h5 text-dark">{ job.title } <br> { job.titletwo }</Link>
            <p class="text-muted mb-0 mt-3">{ job.count } Jobs</p>
          </div>
        </div>
      </div><!--end col-->
      {/each}

    </div><!--end row-->
  </div><!--end container-->
</main>

<style lang="scss" scoped></style>