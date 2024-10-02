<script>
    import Sidebar from '../../components/blogs/sidebar.svelte'
    import detailimg from '../../assets/images/blog/01.jpg';
    import team from '../../assets/images/team/01.jpg';
    import team2 from '../../assets/images/team/02.jpg';
    import team3 from '../../assets/images/team/03.jpg';
    import team4 from '../../assets/images/team/01.jpg';
             
    </script>

<main>
    <div class="container">
        <div class="row g-4">
            <div class="col-lg-8 col-md-7">
                <div class="card border-0 shadow rounded overflow-hidden">

                    <img src={detailimg} alt="">

                    <div class="card-body">
                        <p class="text-muted">The most well-known dummy text is the 'Lorem Ipsum', which is said to have
                            originated in the 16th century. Lorem Ipsum is composed in a pseudo-Latin language which
                            more or less corresponds to 'proper' Latin. It contains a series of real Latin words. This
                            ancient dummy text is also incomprehensible, but it imitates the rhythm of most European
                            languages in Latin script. The advantage of its Latin origin and the relative
                            meaninglessness of Lorum Ipsum is that the text does not attract attention to itself or
                            distract the viewer's attention from the layout.</p>
                        <p class="text-muted">Thus, Lorem Ipsum has only limited suitability as a visual filler for
                            German texts. If the fill text is intended to illustrate the characteristics of different
                            typefaces, it sometimes makes sense to select texts containing the various letters and
                            symbols specific to the output language.</p>

                        <blockquote class="text-center mx-auto blockquote"><i
                                class="mdi mdi-format-quote-open mdi-48px text-muted opacity-2 d-block"></i> The man who
                            comes back through the door in the wall will never be quite the same as the man who went
                            out. <small class="d-block text-muted mt-2">- Jobnova Template</small></blockquote>

                        <p class="text-muted">There is now an abundance of readable dummy texts. These are usually used
                            when a text is required purely to fill a space. These alternatives to the classic Lorem
                            Ipsum texts are often amusing and tell short, funny or nonsensical stories.</p>

                        <a href="#name" class="badge badge-link bg-primary me-1">Minimal</a>
                        <a href="#name" class="badge badge-link bg-primary me-1">Interior</a>
                        <a href="#name" class="badge badge-link bg-primary">Furniture</a>
                    </div>
                </div>

                <div class="card shadow rounded border-0 mt-4">
                    <div class="card-body">
                        <h5 class="card-title mb-0">Comments :</h5>

                        <ul class="media-list list-unstyled mb-0">
                            <li class="mt-4">
                                <div class="d-flex justify-content-between">
                                    <div class="d-flex align-items-center">
                                        <a class="pe-3" href="#name">
                                            <img src={team}
                                                class="img-fluid avatar avatar-md-sm rounded-circle shadow" alt="img">
                                        </a>
                                        <div class="commentor-detail">
                                            <h6 class="mb-0"><a href="#name"
                                                    class="text-dark media-heading">Lorenzo Peterson</a></h6>
                                            <small class="text-muted">15th August, 2021 at 01:25 pm</small>
                                        </div>
                                    </div>
                                    <a href="#name" class="text-muted"><i class="mdi mdi-reply"></i> Reply</a>
                                </div>
                                <div class="mt-3">
                                    <p class="text-muted fst-italic p-3 bg-light rounded">" There are many variations of
                                        passages of Lorem Ipsum available, but the majority have suffered alteration in
                                        some form, by injected humour "</p>
                                </div>
                            </li>

                            <li class="mt-4">
                                <div class="d-flex justify-content-between">
                                    <div class="d-flex align-items-center">
                                        <a class="pe-3" href="#name">
                                            <img src={team2}
                                                class="img-fluid avatar avatar-md-sm rounded-circle shadow" alt="img">
                                        </a>
                                        <div class="commentor-detail">
                                            <h6 class="mb-0"><a href="#name"
                                                    class="media-heading text-dark">Tammy Camacho</a></h6>
                                            <small class="text-muted">15th August, 2021 at 05:44 pm</small>
                                        </div>
                                    </div>
                                    <a href="#name" class="text-muted"><i class="mdi mdi-reply"></i> Reply</a>
                                </div>
                                <div class="mt-3">
                                    <p class="text-muted fst-italic p-3 bg-light rounded">" There are many variations of
                                        passages of Lorem Ipsum available, but the majority have suffered alteration in
                                        some form, by injected humour "</p>
                                </div>
                            </li>

                            <li class="mt-4">
                                <div class="d-flex justify-content-between">
                                    <div class="d-flex align-items-center">
                                        <a class="pe-3" href="#name">
                                            <img src={team3}
                                                class="img-fluid avatar avatar-md-sm rounded-circle shadow" alt="img">
                                        </a>
                                        <div class="commentor-detail">
                                            <h6 class="mb-0"><a href="#name"
                                                    class="media-heading text-dark">Tammy Camacho</a></h6>
                                            <small class="text-muted">16th August, 2021 at 03:44 pm</small>
                                        </div>
                                    </div>
                                    <a href="#name" class="text-muted"><i class="mdi mdi-reply"></i> Reply</a>
                                </div>
                                <div class="mt-3">
                                    <p class="text-muted fst-italic p-3 bg-light rounded">" There are many variations of
                                        passages of Lorem Ipsum available, but the majority have suffered alteration in
                                        some form, by injected humour "</p>
                                </div>

                                <ul class="list-unstyled ps-4 ps-md-5 sub-comment">
                                    <li class="mt-4">
                                        <div class="d-flex justify-content-between">
                                            <div class="d-flex align-items-center">
                                                <a class="pe-3" href="#name">
                                                    <img src={team4}
                                                        class="img-fluid avatar avatar-md-sm rounded-circle shadow"
                                                        alt="img">
                                                </a>
                                                <div class="commentor-detail">
                                                    <h6 class="mb-0"><a href="#name"
                                                            class="text-dark media-heading">Lorenzo Peterson</a></h6>
                                                    <small class="text-muted">17th August, 2021 at 01:25 pm</small>
                                                </div>
                                            </div>
                                            <a href="#name" class="text-muted"><i class="mdi mdi-reply"></i> Reply</a>
                                        </div>
                                        <div class="mt-3">
                                            <p class="text-muted fst-italic p-3 bg-light rounded">" There are many
                                                variations of passages of Lorem Ipsum available, but the majority have
                                                suffered alteration in some form, by injected humour "</p>
                                        </div>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="card shadow rounded mt-4">
                    <div class="card-body">
                        <h5 class="card-title mb-0">Leave A Comment :</h5>

                        <form class="mt-4">
                            <div class="row">
                                <div class="col-md-12">
                                    <div class="mb-3">
                                        <label class="form-label" for="comments">Your Comment</label>
                                        <textarea id="message" placeholder="Your Comment" rows="5" name="message"
                                            class="form-control" required></textarea>
                                    </div>
                                </div><!--end col-->

                                <div class="col-lg-6">
                                    <div class="mb-3">
                                        <label class="form-label" for="name">Name <span class="text-danger">*</span></label>
                                        <input id="name" name="name" type="text" placeholder="Name" class="form-control"
                                            required>
                                    </div>
                                </div><!--end col-->

                                <div class="col-lg-6">
                                    <div class="mb-3">
                                        <label class="form-label" for="email">Your Email <span class="text-danger">*</span></label>
                                        <input id="email" type="email" placeholder="Email" name="email"
                                            class="form-control" required>
                                    </div>
                                </div><!--end col-->

                                <div class="col-md-12">
                                    <div class="send d-grid">
                                        <button type="submit" class="btn btn-primary">Send Message</button>
                                    </div>
                                </div><!--end col-->
                            </div><!--end row-->
                        </form><!--end form-->
                    </div>
                </div>
            </div><!--end col-->

            <!-- START SIDEBAR -->
            <Sidebar />
            <!-- END SIDEBAR -->
        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>