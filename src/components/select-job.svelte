<script>
	import { onMount } from 'svelte';
  import Select from 'svelte-select';
  import feather from 'feather-icons';

  export let selectjob

  onMount(() => {
    feather.replace()
  })

  const items = [
    {value: 'Afghanistan', label: 'Afghanistan'},
    {value: 'Azerbaijan', label: 'Azerbaijan'},
    {value: 'Bahamas', label: 'Bahamas'},
    {value: 'Bahrain', label: 'Bahrain'},
    {value: 'Canada', label: 'Canada'}, 
    {value: 'Cape Verde', label: 'Cape Verde'}, 
    {value: 'Denmark', label: 'Denmark'}, 
    {value: 'Djibouti', label: 'Djibouti'}, 
    {value: 'Eritrea', label: 'Eritrea'}, 
    {value: 'Estonia', label: 'Estonia'}, 
    {value: 'Gambia', label: 'Gambia'} 
  ];
  
  const itemstwo = [
    {value: 'Full Time', label: 'Full Time'},
    {value: 'Part Time', label: 'Part Time'},
    {value: 'Freelancer', label: 'Freelancer'},
    {value: 'Remote Work', label: 'Remote Work'},
    {value: 'Office Work', label: 'Office Work'}, 
  ];

  let location = 'Afghanistan';
  let type = 'Full Time';


</script>

<main>
  <div class={`d-md-flex justify-content-between align-items-center bg-white shadow rounded ${selectjob}`} >
    <form class="card-body text-start">
        <div class="registration-form text-dark text-start">
            <div class="row g-lg-0">
                <div class="col-lg-3 col-md-6 col-12">
                    <div class="mb-3 mb-sm-0">
                        <label class="form-label d-none fs-6" for="search">Search :</label>
                        <div class="filter-search-form position-relative filter-border">
                            <i data-feather="search" class="fea icon-20 icons"></i>
                            <input name="name" type="text" id="job-keyword" class="form-control filter-input-box bg-light border-0" placeholder="Search your keaywords">
                        </div>
                    </div>
                </div><!--end col-->
                
                <div class="col-lg-3 col-md-6 col-12 ">
                    <div class="mb-3 mb-sm-0">
                        <label class="form-label d-none fs-6" for="location">Location:</label>
                        <div class="filter-search-form position-relative filter-border bg-light p-2">
                            <i data-feather="map-pin" class="fea icon-20 icons"></i>
                            <i class="uil uil-angle-down arrow-up"></i>
                            <Select {items} bind:value={location} class="border-0 bg-light ms-3" />
                        </div>
                    </div>
                </div><!--end col-->

                <div class="col-lg-3 col-md-6 col-12">
                    <div class="mb-3 mb-sm-0">
                        <label class="form-label d-none fs-6" for="type">Type :</label>
                        <div class="filter-search-form position-relative filter-border bg-light p-2">
                          <i data-feather="briefcase" class="fea icon-20 icons"></i>
                          <i class="uil uil-angle-down arrow-up"></i>
                          <Select items={itemstwo} bind:value={type} class="border-0 bg-light ms-3 lightbox" />
                      </div>
                    </div>
                </div><!--end col-->

                <div class="col-lg-3 col-md-6 col-12">
                    <input type="submit" id="search" name="search" style="height: 60px;" class="btn btn-primary searchbtn w-100" value="Search">
                </div><!--end col-->
            </div><!--end row-->
        </div>
    </form><!--end form-->
</div>
</main>
