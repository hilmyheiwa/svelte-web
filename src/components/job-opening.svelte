<script>
    import { Link } from "svelte-routing"
    const datas = [
        {
            name: 'Frontend Developer',
            opening: 'Total Openings: 1'
        },
        {
            name: 'Backend Developer',
            opening: 'Total Openings: 3'
        },
        {
            name: 'Web Developer',
            opening: 'Total Openings: 2'
        },
    ]
    </script>

<main>
    <div class="row justify-content-center mb-4 pb-2">
        <div class="col-12">
            <div class="section-title text-center">
                <h4 class="title mb-3">Job Openings</h4>
                <p class="text-muted para-desc mx-auto mb-0">Search all the open positions on the web. Get your own
                    personalized salary estimate. Read reviews on over 30000+ companies worldwide.</p>
            </div>
        </div><!--end col-->
    </div><!--end row-->

    <div class="row justify-content-center">
        {#each datas as item }
        <div class="col-lg-10 col-12 mt-4 pt-2">
            <div class="job-post shadow rounded d-md-flex align-items-center justify-content-between p-4">
                <div class="mb-3 mb-md-0">
                    <Link to="/job-detail-one" class="h5 title text-dark">{ item.name }</Link>
                    <p class="text-muted mt-2 mb-0">{ item.opening}</p>
                </div>
                <Link to="/job-detail-one" class="btn btn-soft-primary">Apply Now <i
                        class="mdi mdi-arrow-right"></i></Link>
            </div>
        </div><!--end col-->
        {/each}
       
    </div><!--end row-->
</main>


<style lang="scss" scoped></style>