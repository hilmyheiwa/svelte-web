<script>
import { Link } from "svelte-routing";

  const categories = [
    { name: 'Human Resource', jobsAvailable: 90, },
    { name: 'It & Networking', jobsAvailable: 90, },
    { name: 'Sales & Marketing', jobsAvailable: 90, },
    { name: 'Accounting', jobsAvailable: 90, },
    { name: 'Delivery Boy', jobsAvailable: 90, },
    { name: 'Data Science', jobsAvailable: 90, },
    { name: 'Project Manager', jobsAvailable: 90, },
    { name: 'Engineering', jobsAvailable: 90, },
    { name: 'Help Center', jobsAvailable: 90, },
    { name: 'Full Stack Developer', jobsAvailable: 90, },
  ]
  </script>

<main>
  <div>
    <div class="row justify-content-center mb-4 pb-2">
      <div class="col-12">
        <div class="section-title text-center">
          <h4 class="title mb-3">Browse by Categories</h4>
          <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
            personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
        </div>
      </div><!--end col-->
    </div><!--end row-->

    <div class="row row-cols-lg-5 row-cols-md-3 row-cols-sm-2 row-cols-1 g-4 mt-0">
      {#each categories as category }
      <div class="col">
        <div class="job-category job-category-two rounded shadow bg-light p-3">
          <h5 class="mb-1">{ category.name }</h5>
          <p class="text-muted para mb-2">{ category.jobsAvailable } Jobs Available</p>
          <Link to="#" class="text-primary fw-medium link">Explore Jobs <i
              class="mdi mdi-arrow-right"></i></Link>
        </div>
      </div><!--end col-->
      {/each}
      
    </div><!--end row-->

    <div class="row mt-4">
      <div class="col-12">
        <div class="text-center">
          <Link to="/job-categories" class="btn btn-link primary text-muted">See More Categories <i
              class="mdi mdi-arrow-right"></i></Link>
        </div>
      </div><!--end col-->
    </div>
  </div>
</main>


<style lang="scss" scoped>
/* your styles here */
</style>