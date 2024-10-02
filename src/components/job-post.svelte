<script>

</script>

<main>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-xl-7 col-lg-8">
                <div class="card border-0">
                    <form class="rounded shadow p-4">
                        <div class="row">
                            <h5 class="mb-3">Job Details:</h5>
                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="title">Job Title :</label>
                                    <input name="subject" id="subject2" class="form-control" placeholder="Title :">
                                </div>
                            </div><!--end col-->
                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="desc">Description :</label>
                                    <textarea name="comments" id="comments2" rows="4" class="form-control"
                                        placeholder="Describe the job :"></textarea>
                                </div>
                            </div><!--end col-->
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="type">Job Type:</label>
                                    <select class="form-control form-select" id="Type">
                                        <option value="WD">Web Designer</option>
                                        <option value="WD">Web Developer</option>
                                        <option value="UI">UI / UX Desinger</option>
                                    </select>
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="job">Job Categories:</label>
                                    <select class="form-control form-select" id="Categories">
                                        <option>All Jobs</option>
                                        <option>Full Time</option>
                                        <option>Half Time</option>
                                        <option>Remote</option>
                                        <option>In Office</option>
                                    </select>
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="salary">Salary:</label>
                                    <select class="form-control form-select" id="Salary">
                                        <option value="HOURL">Hourly</option>
                                        <option value="MONTH">Monthly</option>
                                    </select>
                                </div>
                            </div><!--end col-->

                            <div class="col-md-3">
                                <div class="mb-3 mt-md-4 pt-md-1">
                                    <label class="form-label small fw-bold d-none" for="price"></label>
                                    <div class="input-group mb-3">
                                        <span class="input-group-text border" id="basic-addon1">$</span>
                                        <input type="number" class="form-control" min="1" max="1000" placeholder="Min"
                                            id="MIn" aria-describedby="inputGroupPrepend" required>
                                    </div>
                                </div>
                            </div><!--end col-->

                            <div class="col-md-3">
                                <div class="mb-3 mt-md-4 pt-md-1">
                                    <label class="form-label small fw-bold d-none" for="price"></label>
                                    <div class="input-group mb-3">
                                        <span class="input-group-text border" id="basic-addon1">$</span>
                                        <input type="number" class="form-control" min="1" max="1000" placeholder="Max"
                                            id="Max" aria-describedby="inputGroupPrepend" required>
                                    </div>
                                </div>
                            </div><!--end col-->
                        </div>

                        <div class="row">
                            <h5 class="mb-3">Skill & Experience:</h5>
                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="skill">Skills:</label>
                                    <input name="name" id="skills" type="text" class="form-control"
                                        placeholder="Web Developer">
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="qufc">Qualifications:</label>
                                    <input name="name" id="Qualifications" type="text" class="form-control"
                                        placeholder="Qualifications">
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="exp">Experience:</label>
                                    <input name="name" id="Experience" type="text" class="form-control"
                                        placeholder="Experience">
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="ids">Industry:</label>
                                    <select class="form-control form-select" id="Industry">
                                        <option value="BANK">Banking</option>
                                        <option value="BIO">Biotechnology</option>
                                        <option value="AVI">Aviation</option>
                                    </select>
                                </div>
                            </div><!--end col-->
                        </div>

                        <div class="row">
                            <h5 class="mb-3">Skill & Experience:</h5>
                            <div class="col-12">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="addr">Address:</label>
                                    <input name="name" id="Address" type="text" class="form-control"
                                        placeholder="Address">
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="country">Country:</label>
                                    <select class="form-control form-select" id="Country">
                                        <option value="USA">USA</option>
                                        <option value="CAD">Canada</option>
                                        <option value="CHINA">China</option>
                                    </select>
                                </div>
                            </div><!--end col-->

                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label class="form-label fw-semibold" for="state">State:</label>
                                    <select class="form-control form-select" id="State">
                                        <option value="CAL">California</option>
                                        <option value="TEX">Texas</option>
                                        <option value="FLOR">Florida</option>
                                    </select>
                                </div>
                            </div><!--end col-->

                            <div class="col-12">
                                <div class="card map border-0 rounded mb-3">
                                    <div class="card-body p-0">
                                        <iframe title="YouTube video player"
                                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                                            class="rounded" style="border:0; height: 250px" allowfullscreen></iframe>
                                    </div>
                                </div>
                            </div><!--end col-->
                        </div><!--end row-->

                        <div class="row">
                            <div class="col-12">
                                <input type="submit" id="submit2" name="send" class="submitBnt btn btn-primary"
                                    value="Post Now">
                            </div><!--end col-->
                        </div><!--end row-->
                    </form><!--end form-->
                </div><!--end custom-form-->
            </div>
        </div>
    </div><!--end container-->
</main>


<style lang="scss" scoped></style>