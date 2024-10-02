<script>
    import {  onMount } from 'svelte';
    import image from '../../assets/images/company/lenovo-logo.png';
    import image2 from '../../assets/images/company/lenovo-logo.png';
    import image3 from '../../assets/images/company/lenovo-logo.png';
    import image4 from '../../assets/images/company/lenovo-logo.png';
    import feather from 'feather-icons';
    import company from '../../assets/images/company/1.jpg';
    import company2 from '../../assets/images/company/2.jpg';
    import company3 from '../../assets/images/company/3.jpg';
    import { Link } from 'svelte-routing';
    
    const datas =  [
        {
            id: 1,
            title: 'Software Engineering',
            time: 'Posted 3 Days ago',
            type: 'Full Time',
            salary: '$950 - $1100/mo',
            image: image,
            name: 'Lenovo',
            location: 'Australia'
        },
        {
            id: 2,
            title: 'Web Developer',
            time: 'Posted 4 Days ago',
            type: 'Remote',
            salary: '$2500 - $2600/mo',
            image: image2,
            name: 'Lenovo',
            location: 'USA'
        },
        {
            id: 3,
            title: 'Web Designer',
            time: 'Posted 5 Days ago',
            type: 'Part Time',
            salary: '$250 - $450/mo',
            image: image3,
            name: 'Lenovo',
            location: 'Japan'
        },
        {
            id: 4,
            title: 'HR Manager',
            time: 'Posted 10 Days ago',
            type: 'Full Time',
            salary: '$500 - $750/mo',
            image: image4,
            name: 'Lenovo',
            location: 'India'
        },
    ];
    
    const social = [
        {
            link: 'https://dribbble.com/shreethemes',
            name: 'dribbble'
        },
        {
            link: 'http://linkedin.com/company/shreethemes',
            name: 'linkedin'
        },
        {
            link: 'https://www.facebook.com/shreethemes',
            name: 'facebook'
        },
        {
            link: 'https://www.instagram.com/shreethemes/',
            name: 'instagram'
        },
        {
            link: 'https://twitter.com/shreethemes',
            name: 'twitter'
        },
    ]
    
    onMount(() => {
        feather.replace()
    })
    </script>

<main>
    <div class="row g-4">
        <div class="col-lg-8 col-md-7 col-12">
            <h4 class="mb-4">Company Story:</h4>

            <p class="text-muted">It is a long established fact that a reader will be distracted by the readable content
                of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less
                normal distribution of letters, as opposed.</p>
            <p class="text-muted">Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a
                piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a
                Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words,
                consectetur, from a Lorem Ipsum passage.</p>

            <div class="row g-4">
                <div class="col-12"><img src={company} class="rounded shadow img-fluid"
                        alt=""></div>
                <div class="col-6"><img src={company2} class="rounded shadow img-fluid" alt="">
                </div>
                <div class="col-6"><img src={company3} class="rounded shadow img-fluid" alt="">
                </div>
            </div>

            <h4 class="my-4">Vacancies:</h4>

            <div class="row g-4">
                {#each datas as item}
                <div class="col-lg-6 col-12">
                    <div class="job-post rounded shadow bg-white">
                        <div class="p-4">
                            <Link to={`/job-detail-one/${item.id}`}
                                class="text-dark title h5">{ item.title }</Link>

                            <p class="text-muted d-flex align-items-center small mt-3"><i data-feather="clock"
                                    class="fea icon-sm text-primary me-1"></i>{ item.time }</p>

                            <ul class="list-unstyled d-flex justify-content-between align-items-center mb-0 mt-3">
                                <li class="list-inline-item"><span class="badge bg-soft-primary">{ item.type}</span>
                                </li>
                                <li class="list-inline-item"><span class="text-muted d-flex align-items-center small"><i
                                            data-feather="dollar-sign" class="fea icon-sm text-primary me-1"></i>{
                                                item.salary }</span></li>
                            </ul>
                        </div>
                        <div class="d-flex align-items-center p-4 border-top">
                            <img src={item.image} class="avatar avatar-small rounded shadow p-3 bg-white" alt="">

                            <div class="ms-3">
                                <h6>{ item.name }</h6>
                                <span class="text-muted d-flex align-items-center"><i data-feather="map-pin"
                                        class="fea icon-sm me-1"></i>{ item.location }</span>
                            </div>
                        </div>
                    </div>
                </div>
                {/each}
              
            </div>
        </div><!--end col-->

        <div class="col-lg-4 col-md-5 col-12">
            <div class="card bg-white p-4 rounded shadow sticky-bar">
                <div class="map map-400px border-0">
                    <iframe title="map"
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                        class="rounded" style="border:0" allowfullscreen></iframe>
                </div>

                <div class="mt-3">
                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Founded:</span>
                        <span>1984</span>
                    </div>

                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Founder:</span>
                        <span>Liu Chuanzhi</span>
                    </div>

                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Headquarters:</span>
                        <span>Hong Kong</span>
                    </div>

                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Number of employees:</span>
                        <span>+ 75000</span>
                    </div>

                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Website:</span>
                        <span>www.lenovo.com</span>
                    </div>

                    <div class="d-flex align-items-center justify-content-between mt-2">
                        <span class="text-muted fw-medium">Social:</span>

                        <ul class="list-unstyled social-icon text-sm-end mb-0">
                            {#each social as item}
                            <li class="list-inline-item me-1"><a href={item.link}
                                    target="_blank" class="rounded"><i data-feather={item.name}
                                        class="fea icon-sm align-middle" title="dribbble"></i></a></li>                                
                            {/each}
                        </ul><!--end icon-->
                    </div>
                </div>

                <div class="mt-4 pt-4 border-top">
                    <h5>Get in touch !</h5>
                    <form>
                        <div class="row">
                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="name">Your Name <span
                                            class="text-danger">*</span></label>
                                    <input name="name" id="name" type="text" class="form-control" placeholder="Name :">
                                </div>
                            </div>

                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="email">Your Email <span
                                            class="text-danger">*</span></label>
                                    <input name="email" id="email" type="email" class="form-control"
                                        placeholder="Email :">
                                </div>
                            </div><!--end col-->

                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="subject">Subject</label>
                                    <input name="subject" id="subject" class="form-control" placeholder="Subject :">
                                </div>
                            </div><!--end col-->

                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="comments">Comments <span
                                            class="text-danger">*</span></label>
                                    <textarea name="comments" id="comments" rows="4" class="form-control"
                                        placeholder="Message :"></textarea>
                                </div>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-12">
                                <div class="d-grid">
                                    <button type="submit" id="submit" name="send" class="btn btn-primary">Send
                                        Message</button>
                                </div>
                            </div><!--end col-->
                        </div><!--end row-->
                    </form>
                </div>
            </div>
        </div><!--end col-->
    </div><!--end row-->
</main>



<style lang="scss" scoped></style>