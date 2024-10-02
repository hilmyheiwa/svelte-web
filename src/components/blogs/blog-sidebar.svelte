<script>
    import { Link } from 'svelte-routing';
    import Pagination from '../../components/pagination.svelte';
    import Sidebar from '../../components/blogs/sidebar.svelte'
    import image from '../../assets/images/blog/01.jpg';
    import image2 from '../../assets/images/blog/02.jpg';
    import image3 from '../../assets/images/blog/03.jpg';
    import image4 from '../../assets/images/blog/04.jpg';
    import image5 from '../../assets/images/blog/05.jpg';
    import image6 from '../../assets/images/blog/06.jpg';
    import image7 from '../../assets/images/blog/07.jpg';
    import image8 from '../../assets/images/blog/08.jpg';
    
    const blogs = [
        {
            id: 1,
            image: image,
            name: 'Arts',
            title: '11 Tips to Help You Get New Clients Through Cold Calling',
            company: 'Google',
            nametwo: 'Consultant Business'
        },
        {
            id: 2,
            image: image2,
            name: 'Illustration',
            title: 'DigitalOcean launches first Canadian data centre in Toronto',
            company: 'Facebook',
            nametwo: 'Grow Your Business'
        },
        {
            id: 3,
            image: image3,
            name: 'Music',
            title: 'Using Banner Stands To Increase Trade Show Traffic',
            company: 'Linkedin',
            nametwo: 'Look On The Glorious Balance'
        },
        {
            id: 4,
            image: image4,
            name: 'Arts',
            title: '11 Tips to Help You Get New Clients Through Cold Calling',
            company: 'Google'
        },
        {
            id: 5,
            image: image5,
            name: 'Illustration',
            title: 'DigitalOcean launches first Canadian data centre in Toronto',
            company: 'Facebook'
        },
        {
            id: 6,
            image: image6,
            name: 'Music',
            title: 'Using Banner Stands To Increase Trade Show Traffic',
            company: 'Linkedin'
        },
        {
            id: 7,
            image: image7,
            name: 'Arts',
            title: '11 Tips to Help You Get New Clients Through Cold Calling',
            company: 'Google'
        },
        {
            id: 8,
            image: image8,
            name: 'Illustration',
            title: 'DigitalOcean launches first Canadian data centre in Toronto',
            company: 'Facebook'
        },
       
    ]
    </script>

<main>
    <div class="container">
        <div class="row g-4">
            <div class="col-lg-8 col-md-6 col-12">
                <div class="row g-4">
                    {#each blogs as item }
                    <div class="col-lg-6">
                        <div class="card blog blog-primary shadow rounded overflow-hidden border-0">
                            <div class="card-img blog-image position-relative overflow-hidden rounded-0">
                                <div class="position-relative overflow-hidden">
                                    <img src={item.image} class="img-fluid" alt="">
                                    <div class="card-overlay"></div>
                                </div>
                            </div>

                            <div class="card-body blog-content position-relative p-0">
                                <div class="blog-tag px-4">
                                    <a href="#name" class="badge bg-primary rounded-pill">{ item.name }</a>
                                </div>
                                <div class="p-4">
                                    <ul class="list-unstyled text-muted small mb-2">
                                        <li class="d-inline-flex align-items-center me-2"><i data-feather="calendar"
                                                class="fea icon-ex-sm me-1 text-dark"></i>31st October 2023</li>
                                        <li class="d-inline-flex align-items-center"><i data-feather="clock"
                                                class="fea icon-ex-sm me-1 text-dark"></i>5 min read</li>
                                    </ul>

                                    <Link to={`/blog-detail/${item.id}`} class="title fw-semibold fs-5 text-dark">
                                        {
                                            item.title
                                        }</Link>

                                    <ul
                                        class="list-unstyled d-flex justify-content-between align-items-center text-muted mb-0 mt-3">
                                        <li class="list-inline-item me-2">
                                            <Link to={`/blog-detail/${item.id}`}
                                                class="btn btn-link primary text-dark">Read Now <i
                                                    class="mdi mdi-arrow-right"></i></Link>
                                        </li>
                                        <li class="list-inline-item"><span class="text-dark">By</span> <a href="#name"
                                                class="text-muted link-title">{ item.company }</a></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div><!--end col-->
                    {/each}
                  
                </div><!--end row-->

                <Pagination />
            </div>

            <Sidebar />
        </div>
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>