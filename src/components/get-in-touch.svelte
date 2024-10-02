<script>
    import image from '../assets/images/svg/contact.svg'

</script>

<main>
    <div class="container">
        <div class="row align-items-center">
            <div class="col-md-6">
                <img src={image} class="img-fluid" alt="">
            </div>
            <div class="col-md-6">
                <div class="p-4 rounded shadow ms-lg-5">
                    <h4>Get in touch !</h4>
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
        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>