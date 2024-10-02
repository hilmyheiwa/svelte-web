<script>
    import resumeUrl from '../../assets/images/calvin-carlo-resume.pdf';
    import image from '../../assets/images/company/linkedin.png';
    import image2 from '../../assets/images/company/lenovo-logo.png';

    const social = [
        {
            link: 'https://dribbble.com/shreethemes',
            icon: 'dribbble'
        },
        {
            link: 'http://linkedin.com/company/shreethemes',
            icon: 'linkedin'
        },
        {
            link: 'https://www.facebook.com/shreethemes',
            icon: 'facebook'
        },
        {
            link: 'https://www.instagram.com/shreethemes/',
            icon: 'instagram'
        },
        {
            link: 'https://twitter.com/shreethemes',
            icon: 'twitter'
        },
    ]
    
    const info = [
        {
            name: 'Email:',
            icon: 'mail',
            title: 'thomas@mail.com'
        },
        {
            name: 'D.O.B.:',
            icon: 'gift',
            title: '31st Dec, 1996'
        },
        {
            name: 'Address:',
            icon: 'home',
            title: '15 Razy street'
        },
        {
            name: 'City:',
            icon: 'map-pin',
            title: 'London'
        },
        {
            name: 'Country:',
            icon: 'globe',
            title: 'UK'
        },
        {
            name: 'Mobile:',
            icon: 'phone',
            title: '(+125) 1542-8452'
        },
    ]
    
    const language = [
        {
            name: 'HTML',
            width: '84%'
        },
        {
            name: 'CSS',
            width: '75%'
        },
        {
            name: 'JQuery',
            width: '79%'
        },
        {
            name: 'WordPress',
            width: '79%'
        },
        {
            name: 'Figma',
            width: '85%'
        },
        {
            name: 'Illustration',
            width: '65%'
        },
    ]
    
    </script>

<main>
    <div class="container mt-4">
        <div class="row g-4">
            <div class="col-lg-8 col-md-7 col-12">
                <h5 class="mb-4">Introduction:</h5>

                <p class="text-muted">Obviously I'M Web Developer. Web Developer with over 3 years of experience.
                    Experienced with all stages of the development cycle for dynamic web projects. The as opposed to
                    using 'Content here, content here', making it look like readable English.</p>
                <p class="text-muted">Data Structures and Algorithms are the heart of programming. Initially most of the
                    developers do not realize its importance but when you will start your career in software
                    development, you will find your code is either taking too much time or taking too much space.</p>

                <h5 class="mt-4">Skills:</h5>

                <div class="row">
                    <div class="col-lg-6 col-12">
                        {#each language.slice(0, 3) as item}
                        <div class="progress-box mt-4">
                            <h6 class="font-weight-normal">{ item.name }</h6>
                            <div class="progress">
                                <div class="progress-bar position-relative bg-primary" style={` width: ${item.width} `}>
                                    <div class="progress-value d-block text-dark h6">{ item.width }</div>
                                </div>
                            </div>
                        </div><!--end process box-->
                        {/each}
                      
                    </div><!--end col-->

                    <div class="col-lg-6 col-12">
                        {#each language.slice(3, 6) as item}
                        <div class="progress-box mt-4">
                            <h6 class="font-weight-normal">{ item.name }</h6>
                            <div class="progress">
                                <div class="progress-bar position-relative bg-primary" style={ `width: ${item.width}` }>
                                    <div class="progress-value d-block text-dark h6">{ item.width }</div>
                                </div>
                            </div>
                        </div><!--end process box-->
                        {/each}
                    
                    </div><!--end col-->
                </div><!--end row-->

                <h5 class="mt-4">Experience:</h5>

                <div class="row">
                    <div class="col-12 mt-4">
                        <div class="d-flex">
                            <div class="text-center">
                                <img src={image}
                                    class="avatar avatar-small bg-white shadow p-2 rounded" alt="">
                                <h6 class="text-muted mt-2 mb-0">2019-22</h6>
                            </div>

                            <div class="ms-3">
                                <h6 class="mb-0">Full Stack Developer</h6>
                                <p class="text-muted">Linkedin - U.S.A.</p>
                                <p class="text-muted mb-0">It seems that only fragments of the original text remain in
                                    the Lorem Ipsum texts used today. One may speculate that over the course of time
                                    certain letters were added or deleted at various positions within the text.</p>
                            </div>
                        </div>
                    </div><!--end col-->

                    <div class="col-12 mt-4">
                        <div class="d-flex">
                            <div class="text-center">
                                <img src={image2}
                                    class="avatar avatar-small bg-white shadow p-2 rounded" alt="">
                                <h6 class="text-muted mt-2 mb-0">2017-19</h6>
                            </div>

                            <div class="ms-3">
                                <h6 class="mb-0">Back-end Developer</h6>
                                <p class="text-muted">Lenovo - China</p>
                                <p class="text-muted mb-0">It seems that only fragments of the original text remain in
                                    the Lorem Ipsum texts used today. One may speculate that over the course of time
                                    certain letters were added or deleted at various positions within the text.</p>
                            </div>
                        </div>
                    </div><!--end col-->
                </div><!--end row-->

                <div class="p-4 rounded shadow mt-4">
                    <h5>Get in touch !</h5>
                    <form>
                        <div class="row">
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="name">Your Name <span
                                            class="text-danger">*</span></label>
                                    <input name="name" id="name" type="text" class="form-control" placeholder="Name :">
                                </div>
                            </div>

                            <div class="col-md-6">
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
            </div><!--end col-->

            <div class="col-lg-4 col-md-5 col-12">
                <div class="card bg-light p-4 rounded shadow sticky-bar">
                    <h5 class="mb-0">Personal Detail:</h5>
                    <div class="mt-3">
                        {#each info as item }
                        <div
                        class="d-flex align-items-center justify-content-between mt-3">
                        <span class="d-inline-flex align-items-center text-muted fw-medium"><i
                                data-feather={item.icon} class="fea icon-sm me-2"></i> { item.name }</span>
                        <span class="fw-medium">{ item.title }</span>
                    </div>
                        {/each}
                        

                        <div class="d-flex align-items-center justify-content-between mt-3">
                            <span class="text-muted fw-medium">Social:</span>

                            <ul class="list-unstyled social-icon text-sm-end mb-0">
                                {#each social as item}
                                <li class="list-inline-item me-1"><a
                                    href={item.link} target="_blank" class="rounded"><i data-feather={item.icon}
                                        class="fea icon-sm align-middle" title="dribbble"></i></a></li>
                                {/each}
                               
                            </ul><!--end icon-->
                        </div>

                        <div class="p-3 rounded shadow bg-white mt-2">
                            <div class="d-flex align-items-center mb-2">
                                <i data-feather="file-text" class="fea icon-md"></i>
                                <h6 class="mb-0 ms-2">calvin-carlo-resume.pdf</h6>
                            </div>

                            <a href={resumeUrl} class="btn btn-primary w-100" target="_blank"
                                download="calvin-carlo-resume.pdf">
                                <i data-feather="download" class="fea icon-sm me-1"></i> Download CV
                            </a>
                        </div>
                    </div>
                </div>
            </div><!--end col-->
        </div><!--end row-->
    </div><!--end container-->
</main>


<style lang="scss" scoped></style>