<script>
    const datas = [
        "One disadvantage of Lorum Ipsum is that in Latin certain letters appear more frequently than others - which creates a distinct visual impression. Moreover, in Latin only words at the beginning of sentences are capitalized.",
        "This means that Lorem Ipsum cannot accurately represent, for example, German, in which all nouns are capitalized. Thus, Lorem Ipsum has only limited suitability as a visual filler for German texts. If the fill text is intended to illustrate the characteristics of different typefaces.",
        "It sometimes makes sense to select texts containing the various letters and symbols specific to the output language.",
        "Participate in requirements analysis",
        "Write clean, scalable code using C# and .NET frameworks",
        "Test and deploy applications and systems",
        "Revise, update, refactor and debug code",
        "Improve existing software",
        "Develop documentation throughout the software development life cycle (SDLC)",
        "Serve as an expert on applications and provide technical support",
        "Proven experience as a .NET Developer or Application Developer",
        "good understanding of SQL and Relational Databases, specifically Microsoft SQL Server.",
        "Experience designing, developing and creating RESTful web services and APIs",
        "Basic know how of Agile process and practices",
        "Good understanding of object-oriented programming.",
        "Good understanding of concurrent programming.",
        "Sound knowledge of application architecture and design.",
        "Excellent problem solving and analytical skills",
    ];

    let data = {
        name: "Lenovo",
        type: "Full Time",
        city: "Beijing, China",
        title: "Back-end Developer",
    };

</script>

<main>
    <div class="container">
        <div class="row g-4">
            <div class="col-lg-4 col-md-6 col-12">
                <div class="card bg-white rounded shadow sticky-bar">
                    <div class="p-4">
                        <h5 class="mb-0">Job Information</h5>
                    </div>

                    <div class="card-body p-4 border-top">
                        <div class="d-flex widget align-items-center">
                            <i data-feather="layout" class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Company Name:</h6>
                                <small class="text-primary mb-0"
                                    >{data.name ? data.name : "Lenovo"}</small
                                >
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i
                                data-feather="user-check"
                                class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">
                                    Employee Type:
                                </h6>
                                <small class="text-primary mb-0"
                                    >{data.type
                                        ? data.type
                                        : "Full Time"}</small
                                >
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i
                                data-feather="map-pin"
                                class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Location:</h6>
                                <small class="text-primary mb-0"
                                    >{data.city
                                        ? data.city
                                        : "Beijing, China"}</small
                                >
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i
                                data-feather="monitor"
                                class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Job Type:</h6>
                                <small class="text-primary mb-0"
                                    >{data.title
                                        ? data.title
                                        : "Back-end Developer"}</small
                                >
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i
                                data-feather="briefcase"
                                class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Experience:</h6>
                                <small class="text-primary mb-0">+2 Year</small>
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i data-feather="book" class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">
                                    Qualifications:
                                </h6>
                                <small class="text-primary mb-0">MSCIT</small>
                            </div>
                        </div>

                        <div class="d-flex widget align-items-centermt-3 mt-3">
                            <i
                                data-feather="dollar-sign"
                                class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Salary:</h6>
                                <small class="text-primary mb-0"
                                    >+50k to 70k</small
                                >
                            </div>
                        </div>

                        <div class="d-flex widget align-items-center mt-3">
                            <i data-feather="clock" class="fea icon-ex-md me-3"
                            ></i>
                            <div class="flex-1">
                                <h6 class="widget-title mb-0">Date posted:</h6>
                                <small class="text-primary mb-0"
                                    >5th Sep, 2021</small
                                >
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-lg-8 col-md-6 col-12">
                <h5>Job Description:</h5>
                {#each datas.slice(0, 3) as item}
                    <p class="text-muted">{item}</p>
                {/each}

                <h5 class="mt-4">Responsibilities and Duties:</h5>
                <p class="text-muted">
                    It sometimes makes sense to select texts containing the
                    various letters and symbols specific to the output language.
                </p>
                <ul class="list-unstyled">
                    {#each datas.slice(3, 10) as item}
                        <li class="text-muted mt-2">
                            <i
                                data-feather="arrow-right"
                                class="fea icon-sm text-primary me-2"
                            ></i>{item}
                        </li>
                    {/each}
                </ul>

                <h5 class="mt-4">
                    Required Experience, Skills and Qualifications:
                </h5>
                <p class="text-muted">
                    It sometimes makes sense to select texts containing the
                    various letters and symbols specific to the output language.
                </p>
                <ul class="list-unstyled">
                    {#each datas.slice(10, 18) as item}
                        <li class="text-muted mt-2">
                            <i
                                data-feather="arrow-right"
                                class="fea icon-sm text-primary me-2"
                            ></i>{item}
                        </li>
                    {/each}
                </ul>

                <div class="mt-4">
                    <a href="/job-apply" class="btn btn-outline-primary"
                        >Apply Now <i class="mdi mdi-send"></i></a
                    >
                </div>
            </div>
        </div>
    </div>
</main>

<style lang="scss" scoped>
</style>
