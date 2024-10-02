<script>
</script>

<main>
    <div class="row">
        <div class="col-12">
            <div class="rounded shadow p-4">
                <form>
                    <h5>Personal Detail :</h5>
                    <div class="row mt-4">
                        <div class="col-md-6">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="first-name"
                                    >First Name:<span class="text-danger"
                                        >*</span
                                    ></label
                                >
                                <input
                                    name="name"
                                    id="firstname"
                                    type="text"
                                    class="form-control"
                                    placeholder="First Name :"
                                />
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-md-6">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="last-name"
                                    >Last Name:<span class="text-danger">*</span
                                    ></label
                                >
                                <input
                                    name="name"
                                    id="lastname"
                                    type="text"
                                    class="form-control"
                                    placeholder="Last Name :"
                                />
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-md-6">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="email"
                                    >Your Email:<span class="text-danger"
                                        >*</span
                                    ></label
                                >
                                <input
                                    name="email"
                                    id="email2"
                                    type="email"
                                    class="form-control"
                                    placeholder="Your email :"
                                />
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-md-6">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="occupation"
                                    >Occupation:</label
                                >
                                <select
                                    class="form-control form-select"
                                    id="Type"
                                >
                                    <option value="WD">Web Designer</option>
                                    <option value="WD">Web Developer</option>
                                    <option value="UI">UI / UX Desinger</option>
                                </select>
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-md-6">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="location"
                                    >Location:</label
                                >
                                <select
                                    class="form-control form-select"
                                    id="Country"
                                >
                                    <option value="USA">USA</option>
                                    <option value="CAD">Canada</option>
                                    <option value="CHINA">China</option>
                                </select>
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-md-6">
                            <div class="mb-3">
                                <label
                                    for="formFile"
                                    class="form-label fw-semibold"
                                    >Upload Your Cv / Resume :</label
                                >
                                <input
                                    class="form-control"
                                    type="file"
                                    id="formFile"
                                />
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-12">
                            <div class="mb-3">
                                <label class="form-label fw-semibold" for="introduction"
                                    >Introduction :</label
                                >
                                <textarea
                                    name="comments"
                                    id="comments2"
                                    rows="4"
                                    class="form-control"
                                    placeholder="Introduction :"
                                ></textarea>
                            </div>
                        </div>
                        <!--end col-->

                        <div class="col-12">
                            <input
                                type="submit"
                                id="submit2"
                                name="send"
                                class="submitBnt btn btn-primary"
                                value="Save Changes"
                            />
                        </div>
                        <!--end col-->
                    </div>
                </form>
            </div>

            <div class="rounded shadow p-4 mt-4">
                <form>
                    <div class="row">
                        <div class="col-md-6 mt-4 pt-2">
                            <h5>Contact Info :</h5>

                            <form>
                                <div class="row mt-4">
                                    <div class="col-lg-12">
                                        <div class="mb-3">
                                            <label 
                                                class="form-label fw-semibold" for="phone"
                                                >Phone No. :</label
                                            >
                                            <input
                                                name="number"
                                                id="number"
                                                type="number"
                                                class="form-control"
                                                placeholder="Phone :"
                                            />
                                        </div>
                                    </div>
                                    <!--end col-->

                                    <div class="col-lg-12">
                                        <div class="mb-3">
                                            <label
                                                class="form-label fw-semibold" for="website"
                                                >Website :</label
                                            >
                                            <input
                                                name="url"
                                                id="url"
                                                type="url"
                                                class="form-control"
                                                placeholder="Url :"
                                            />
                                        </div>
                                    </div>
                                    <!--end col-->

                                    <div class="col-lg-12 mt-2 mb-0">
                                        <button class="btn btn-primary"
                                            >Add</button
                                        >
                                    </div>
                                    <!--end col-->
                                </div>
                                <!--end row-->
                            </form>
                        </div>
                        <!--end col-->

                        <div class="col-md-6 mt-4 pt-2">
                            <h5>Change password :</h5>
                            <form>
                                <div class="row mt-4">
                                    <div class="col-lg-12">
                                        <div class="mb-3">
                                            <label
                                                class="form-label fw-semibold" for="old-password"
                                                >Old password :</label
                                            >
                                            <input
                                                type="password"
                                                class="form-control"
                                                placeholder="Old password"
                                                required
                                            />
                                        </div>
                                    </div>
                                    <!--end col-->

                                    <div class="col-lg-12">
                                        <div class="mb-3">
                                            <label
                                                class="form-label fw-semibold" for="new-password"
                                                >New password :</label
                                            >
                                            <input
                                                type="password"
                                                class="form-control"
                                                placeholder="New password"
                                                required
                                            />
                                        </div>
                                    </div>
                                    <!--end col-->

                                    <div class="col-lg-12">
                                        <div class="mb-3">
                                            <label for="password"
                                                class="form-label fw-semibold"
                                                >Re-type New password :</label
                                            >
                                            <input
                                                type="password"
                                                class="form-control"
                                                placeholder="Re-type New password"
                                                required
                                            />
                                        </div>
                                    </div>
                                    <!--end col-->

                                    <div class="col-lg-12 mt-2 mb-0">
                                        <button class="btn btn-primary"
                                            >Save password</button
                                        >
                                    </div>
                                    <!--end col-->
                                </div>
                                <!--end row-->
                            </form>
                        </div>
                        <!--end col-->
                    </div>
                </form>
            </div>

            <div class="rounded shadow p-4 mt-4">
                <form>
                    <div class="row">
                        <div class="col-lg-6">
                            <h5>Account Notifications :</h5>

                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">When someone mentions me</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        id="noti1"
                                    />
                                    <label class="form-check-label" for="noti1"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">When someone follows me</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        checked
                                        id="noti2"
                                    />
                                    <label class="form-check-label" for="noti2"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">When shares my activity</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        id="noti3"
                                    />
                                    <label class="form-check-label" for="noti3"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">When someone messages me</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        id="noti4"
                                    />
                                    <label class="form-check-label" for="noti4"
                                    ></label>
                                </div>
                            </div>
                        </div>

                        <div class="col-lg-6">
                            <h5>Marketing Notifications :</h5>

                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">
                                    There is a sale or promotion
                                </h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        id="noti5"
                                    />
                                    <label class="form-check-label" for="noti5"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">Company news</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        id="noti6"
                                    />
                                    <label class="form-check-label" for="noti6"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">Weekly jobs</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        checked
                                        id="noti7"
                                    />
                                    <label class="form-check-label" for="noti7"
                                    ></label>
                                </div>
                            </div>
                            <div class="d-flex justify-content-between mt-4">
                                <h6 class="mb-0">Unsubscribe News</h6>
                                <div class="form-check">
                                    <input
                                        class="form-check-input"
                                        type="checkbox"
                                        value=""
                                        checked
                                        id="noti8"
                                    />
                                    <label class="form-check-label" for="noti8"
                                    ></label>
                                </div>
                            </div>
                        </div>
                    </div>
                </form>
            </div>

            <div class="rounded shadow p-4 mt-4">
                <form>
                    <h5 class="text-danger">Delete Account :</h5>
                    <div class="row mt-4">
                        <h6 class="mb-0">
                            Do you want to delete the account? Please press
                            below "Delete" button
                        </h6>
                        <div class="mt-4">
                            <button class="btn btn-danger"
                                >Delete Account</button
                            >
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</main>

<style lang="scss" scoped></style>
