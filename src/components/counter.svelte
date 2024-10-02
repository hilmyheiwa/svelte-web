
<script>
  
import CountUp  from 'svelte-countup';

</script>

<main>
    <div class="container">
        <div class="row g-4">
          <div class="col-md-4">
            <div class="counter-box text-center">
              <h1 class="fw-bold d-flex justify-content-center">
                <span class="counter-value">
                  <CountUp  value={1548} />K+
                </span>
              </h1>
              <h6 class="counter-head text-muted text-uppercase">Job Fulfillment</h6>
            </div>
          </div>
      
          <div class="col-md-4">
            <div class="counter-box text-center">
              <h1 class="fw-bold d-flex justify-content-center">
                <span class="counter-value">
                  <CountUp value={25}/>+
                </span>
              </h1>
              <h6 class="counter-head text-muted text-uppercase">Branches</h6>
            </div>
          </div>
      
          <div class="col-md-4">
            <div class="counter-box text-center">
              <h1 class="fw-bold d-flex justify-content-center">
                <span class="counter-value">
                  <CountUp value={9}/>+
                </span>
              </h1>
              <h6 class="counter-head text-muted text-uppercase">Years Experience</h6>
            </div>
          </div>
        </div>
      </div>
</main>

<style lang="scss" scoped></style>