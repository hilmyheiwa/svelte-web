<script>
import image from '../../assets/images/blog/01.jpg';
import image2 from '../../assets/images/blog/02.jpg';
import image3 from '../../assets/images/blog/03.jpg';

const tags = ['Business', 'Finance', 'Marketing', 'Fashion', 'Bride', 'Lifestyle', 'Travel', 'Beauty', 'Video', 'Audio'];

const blogs = [
    {
        id: 1,
        image: image,
        nametwo: 'Consultant Business'
    },
    {
        id: 2,
        image: image2,
        nametwo: 'Grow Your Business'
    },
    {
        id: 3,
        image: image3,
        nametwo: 'Look On The Glorious Balance'
    },
]

</script>

    <div class="col-lg-4 col-md-6 col-12">
        <div class="card bg-white p-4 rounded shadow sticky-bar">
            <!-- SEARCH -->
            <div>
                <h6 class="pt-2 pb-2 bg-light rounded text-center">Search</h6>

                <div class="search-bar mt-4">
                    <div id="itemSearch2" class="menu-search mb-0">
                        <form role="search" method="get" id="searchItemform2" class="searchform">
                            <input type="text" class="form-control rounded border" name="s" id="searchItem2"
                                placeholder="Search...">
                            <input type="submit" id="searchItemsubmit2" value="Search">
                        </form>
                    </div>
                </div>
            </div>
            <!-- SEARCH -->

            <!-- RECENT POST -->
            <div class="mt-4 pt-2">
                <h6 class="pt-2 pb-2 bg-light rounded text-center">Recent Post</h6>
                <div class="mt-4">
                    {#each blogs.slice(0, 3) as item, index}
                    <div class={`blog blog-primary d-flex align-items-center ${index > 0? 'mt-3' : ''}`}>
                      <img src={item.image} class="avatar avatar-small rounded" style="width: auto;" alt="">
                      <div class="flex-1 ms-3">
                        <a href="#name" class="d-block title text-dark fw-medium">{item.nametwo}</a>
                        <span class="text-muted small">31st October 2023</span>
                      </div>
                    </div>
                  {/each}
                </div>
            </div>
            <!-- RECENT POST -->

            <!-- TAG CLOUDS -->
            <div class="mt-4 pt-2 text-center">
                <h6 class="pt-2 pb-2 bg-light rounded">Tags Cloud</h6>
                <ul class="tagcloud list-unstyled mt-4">
                    {#each tags as item}
                    <li class="d-inline-flex m-1"><a href="#name"
                        class="rounded fw-medium text-dark py-1 px-2">{ item }</a></li>
                    {/each}
              </ul>
            </div>
            <!-- TAG CLOUDS -->
        </div>
    </div><!--end col-->

<style lang="scss" scoped></style>