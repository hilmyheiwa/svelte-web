<script>
    import { Link } from "svelte-routing";
    import logodark from "../assets/images/logo-dark.png";
    import logowhite from "../assets/images/logo-white.png";
    import logolight from "../assets/images/logo-light.png";
    import teams from "../assets/images/team/01.jpg";
    import { onMount, onDestroy } from "svelte";
    import feather from "feather-icons";

    export let logoLight;
    export let logoDark;
    export let navLight;

    let activeIndex = "";
    let navbar;
    let scrollY = 0;
    let openMenu = null;
    let menu = null;
    let toggle = true;

    onMount(() => {
        activeIndex = window.location.pathname;
        window.addEventListener("popstate", () => {
            activeIndex = window.location.pathname;
        });
        navbar = document.getElementById("topnav");
        feather.replace();
        scrollToTop()
    });

    function submenu(item) {
        menu = !menu;
        openMenu = item;
    }

    const handler = () => {
        toggle = !toggle;
    };

    function handleScroll() {
    if (scrollY >= 50) {
      navbar.classList.add("nav-sticky");
    } else {
      navbar.classList.remove("nav-sticky");
    }
  }

  window.addEventListener('scroll', () => {
    scrollY = window.scrollY;
    handleScroll();
  });

  const scrollToTop = () => {
    window.scrollTo({ top: 0, behavior: "smooth" })
}

  onDestroy(() => {
    window.removeEventListener('scroll', () => {
      scrollY = window.scrollY;
      handleScroll();
    });
  });
</script>

<main>
    <header id="topnav" class="defaultscroll sticky">
        <div class="container">
    
            {#if logoLight}
            <a class="logo" href="/">
              <span class="logo-light-mode">
                <img src={logodark} class="l-dark" alt="" />
                <img src={logolight} class="l-light" alt="" />
              </span>
              <img src={logolight} class="logo-dark-mode" alt="" />
            </a>
          {:else if logoDark}
            <a class="logo" href="/">
              <img src={logodark} class="logo-light-mode" alt="" />
              <img src={logolight} class="logo-dark-mode" alt="" />
            </a>
          {:else}
            <a class="logo" href="/">
              <span class="logo-light-mode">
                <img src={logodark} class="l-dark" alt="" />
                <img src={logowhite} class="l-light" alt="" />
              </span>
              <img src={logowhite} class="logo-dark-mode" alt="" />
            </a>
          {/if}

            <div class="menu-extras" >
                <div class="menu-item">
                    <a
                        class="navbar-toggle"
                        id="isToggle"
                        class:open={toggle === false}
                    >
                        <div class="lines" on:click={handler}>
                            <span></span>
                            <span></span>
                            <span></span>
                        </div>
                    </a>
                </div>
            </div>

            <ul class="buy-button list-inline mb-0">
                <li class="list-inline-item ps-1 mb-0">
                    <div class="dropdown">
                        <button
                            type="button"
                            class="dropdown-toggle btn btn-sm btn-icon btn-pills btn-primary"
                            data-bs-toggle="dropdown"
                            aria-haspopup="true"
                            aria-expanded="false"
                        >
                            <i data-feather="search" class="icons"></i>
                        </button>
                        <div
                            class="dropdown-menu dd-menu dropdown-menu-end bg-white rounded border-0 mt-3 p-0"
                            style="width: 240px;"
                        >
                            <div class="search-bar">
                                <div id="itemSearch" class="menu-search mb-0">
                                    <form
                                        role="search"
                                        method="get"
                                        id="searchItemform"
                                        class="searchform"
                                    >
                                        <input
                                            type="text"
                                            class="form-control rounded border"
                                            name="s"
                                            id="searchItem"
                                            placeholder="Search..."
                                        />
                                        <input
                                            type="submit"
                                            id="searchItemsubmit"
                                            value="Search"
                                        />
                                    </form>
                                </div>
                            </div>
                        </div>
                    </div>
                </li>

                <li class="list-inline-item ps-1 mb-0">
                    <div class="dropdown dropdown-primary">
                        <button
                            type="button"
                            class="dropdown-toggle btn btn-sm btn-icon btn-pills btn-primary"
                            data-bs-toggle="dropdown"
                            aria-haspopup="true"
                            aria-expanded="false"
                        >
                            <img
                                src={teams}
                                class="img-fluid rounded-pill"
                                alt=""
                            />
                        </button>
                        <div
                            class="dropdown-menu dd-menu dropdown-menu-end bg-white rounded shadow border-0 mt-3"
                        >
                            <Link
                                to="/candidate-profile"
                                class="dropdown-item fw-medium fs-6"
                                ><i
                                    data-feather="user"
                                    class="fea icon-sm me-2 align-middle"
                                ></i>Profile</Link
                            >
                            <Link
                                to="/candidate-profile-setting"
                                class="dropdown-item fw-medium fs-6"
                                ><i
                                    data-feather="settings"
                                    class="fea icon-sm me-2 align-middle"
                                ></i>Settings</Link
                            >
                            <div class="dropdown-divider border-top"></div>
                            <Link
                                to="/lock-screen"
                                class="dropdown-item fw-medium fs-6"
                                ><i
                                    data-feather="lock"
                                    class="fea icon-sm me-2 align-middle"
                                ></i>Lockscreen</Link
                            >
                            <Link
                                to="/login"
                                class="dropdown-item fw-medium fs-6"
                                ><i
                                    data-feather="log-out"
                                    class="fea icon-sm me-2 align-middle"
                                ></i>Logout</Link
                            >
                        </div>
                    </div>
                </li>
            </ul>

            <div id="navigation" class:d-block={toggle === false}>
                <!-- Navigation Menu-->
                <ul class={`navigation-menu nav-right ${navLight}`}>
                    <li
                        class:active={[
                            "/home",
                            "/",
                            "/index-two",
                            "/index-three",
                        ].includes(activeIndex)}
                        class="has-submenu parent-menu-item"
                    >
                        <a
                            href="#home"
                            on:click={() =>
                                submenu(openMenu === "/home" ? "" : "/home")}
                            >Home</a
                        ><span class="menu-arrow"></span>
                        <ul class="submenu" class:open={openMenu === "/home"}>
                            <li class:active={activeIndex === "/"}>
                                <Link to="/" class="sub-menu-item"
                                    >Hero One</Link
                                >
                            </li>
                            <li class:active={activeIndex === "/index-two"}>
                                <Link to="/index-two" class="sub-menu-item"
                                    >Hero Two</Link
                                >
                            </li>
                            <li class:active={activeIndex === "/index-three"}>
                                <Link to="/index-three" class="sub-menu-item"
                                    >Hero Three</Link
                                >
                            </li>
                        </ul>
                    </li>

                    <li
                        class:active={[
                            "/jobs",
                            "/job-categories",
                            "/job-grid-one",
                            "/job-grid-two",
                            "/job-grid-three",
                            "/job-grid-four",
                            "/job-list-one",
                            "/job-list-two",
                            "/job-detail-one",
                            "/job-detail-two",
                            "/job-detail-three",
                            "/job-apply",
                            "/job-post",
                            "/career"
                        ].includes(activeIndex)}
                        class="has-submenu parent-parent-menu-item"
                    >
                        <a
                            href="#jobs"
                            on:click={() =>
                                submenu(openMenu === "/jobs" ? "" : "/jobs")}
                        >
                            Jobs
                        </a><span class="menu-arrow"></span>
                        <ul
                            class="submenu"
                            class:open={[
                                "/jobs",
                                "/jobgrid",
                                "/joblist",
                                "/jobdetail",
                            ].includes(openMenu)}
                        >
                            <li
                                class:active={activeIndex === "/job-categories"
                                    ? "active"
                                    : ""}
                            >
                                <Link to="/job-categories" class="sub-menu-item"
                                    >Job Categories</Link
                                >
                            </li>

                            <li
                                class:active={[
                                    "/jobgrid",
                                    "/job-grid-one",
                                    "/job-grid-two",
                                    "/job-grid-three",
                                    "/job-grid-four",
                                ].includes(activeIndex)}
                                class="has-submenu parent-menu-item"
                            >
                                <a
                                    href="#grid"
                                    on:click={() =>
                                        submenu(
                                            openMenu === "/jobgrid"
                                                ? ""
                                                : "/jobgrid",
                                        )}
                                >
                                    Job Grids
                                </a><span class="submenu-arrow"></span>
                                <ul
                                    class="submenu"
                                    class:open={openMenu === "/jobgrid"}
                                >
                                    <li
                                        class:active={activeIndex ===
                                            "/job-grid-one"}
                                    >
                                        <Link
                                            to="/job-grid-one"
                                            class="sub-menu-item"
                                            >Job Grid One</Link
                                        >
                                    </li>
                                    <li
                                        class:active={activeIndex ===
                                            "/job-grid-two"}
                                    >
                                        <Link
                                            to="/job-grid-two"
                                            class="sub-menu-item"
                                            >Job Grid Two</Link
                                        >
                                    </li>
                                    <li
                                        class:active={activeIndex ===
                                            "/job-grid-three"}
                                    >
                                        <Link
                                            to="/job-grid-three"
                                            class="sub-menu-item"
                                            >Job Grid Three</Link
                                        >
                                    </li>
                                    <li>
                                        <Link
                                            to="/job-grid-four"
                                            class="sub-menu-item"
                                            >Job Grid Four
                                        </Link>
                                    </li>
                                </ul>
                            </li>

                            <li
                                class:active={[
                                    "/joblist",
                                    "/job-list-one",
                                    "/job-list-two",
                                ].includes(activeIndex)}
                                class="has-submenu parent-menu-item"
                            >
                                <a
                                    href="#list"
                                    on:click={() =>
                                        submenu(
                                            openMenu === "/joblist"
                                                ? ""
                                                : "/joblist",
                                        )}
                                >
                                    Job Lists
                                </a><span class="submenu-arrow"></span>
                                <ul
                                    class="submenu"
                                    class:open={openMenu === "/joblist"}
                                >
                                    <li
                                        class:active={activeIndex ===
                                            "/job-list-one"}
                                    >
                                        <Link
                                            to="/job-list-one"
                                            class="sub-menu-item"
                                            >Job List One</Link
                                        >
                                    </li>
                                    <li
                                        class:active={activeIndex ===
                                            "/job-list-two"}
                                    >
                                        <Link
                                            to="/job-list-two"
                                            class="sub-menu-item"
                                            >Job List Two</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={['/jobdetail', '/job-detail-one', '/job-detail-two', '/job-detail-three'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#detail" on:click={() => submenu(openMenu === '/jobdetail' ? '' : '/jobdetail')}> Job Detail </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/jobdetail'} class="submenu">
                                    <li class:active={activeIndex === '/job-detail-one'}>
                                        <Link
                                            to="/job-detail-one"
                                            class="sub-menu-item"
                                            >Job Detail One</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/job-detail-two'}>
                                        <Link
                                            to="/job-detail-two"
                                            class="sub-menu-item"
                                            >Job Detail Two</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/job-detail-three'}>
                                        <Link
                                            to="/job-detail-three"
                                            class="sub-menu-item"
                                            >Job Detail Three</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={activeIndex === '/job-apply'}>
                                <Link to="/job-apply" class="sub-menu-item"
                                    >Job Apply</Link
                                >
                            </li>

                            <li class:active={activeIndex === '/job-post'}>
                                <Link to="/job-post" class="sub-menu-item"
                                    >Job Post
                            </Link>
                            </li>

                            <li class:active={activeIndex === '/career'}>
                                <Link to="/career" class="sub-menu-item"
                                    >Career
                            </Link>
                            </li>
                        </ul>
                    </li>

                    <li class:active={['/employer', '/employers', '/employer-profile'].includes(activeIndex)} class="has-submenu parent-menu-item">
                        <a href="#employer" on:click={() => submenu(openMenu === '/employer' ? '' : '/employer')}>Employers</a><span class="menu-arrow"
                        ></span>
                        <ul class="submenu" class:open={openMenu === '/employer'}>
                            <li class:active={activeIndex === '/employers'}>
                                <Link to="/employers" class="sub-menu-item"
                                    >Employers</Link
                                >
                            </li>
                            <li class:active={activeIndex === '/employer-profile'}>
                                <Link
                                    to="/employer-profile"
                                    class="sub-menu-item">Employer Profile</Link
                                >
                            </li>
                        </ul>
                    </li>

                    <li class:active={['/candidate', '/candidates', '/candidate-profile', '/candidate-profile-setting'].includes(activeIndex)} class="has-submenu parent-menu-item">
                        <a href="#candidate" on:click={()=> submenu(openMenu === '/candidate' ? '' : '/candidate')}>Candidates</a><span class="menu-arrow"
                        ></span>
                        <ul class="submenu" class:open={openMenu === '/candidate'}>
                            <li class:active={activeIndex === '/candidates'}>
                                <Link to="/candidates" class="sub-menu-item"
                                    >Candidates</Link
                                >
                            </li>
                            <li class:active={activeIndex === '/candidate-profile'}>
                                <Link
                                    to="/candidate-profile"
                                    class="sub-menu-item">Candidate Profile</Link
                                >
                            </li>
                            <li class:active={activeIndex === '/candidate-profile-setting'}>
                                <Link
                                    to="/candidate-profile-setting"
                                    class="sub-menu-item">Profile Setting</Link
                                >
                            </li>
                        </ul>
                    </li>

                    <li class:active={['/pages', '/aboutus', '/services', '/pricing', '/helpcenter-overview', '/helpcenter-faqs', '/helpcenter-guides', '/helpcenter-support', '/blogs', '/blog-sidebar', '/blog-detail', '/login', '/signup', '/reset-password', '/lock-screen', '/terms', '/privacy', '/comingsoon', '/maintenance', '/error'].includes(activeIndex)} class="has-submenu parent-parent-menu-item">
                        <a href="#pages" on:click={() => submenu(openMenu === '/pages' ? '' : '/pages')}>Pages</a><span class="menu-arrow"></span>
                        <ul class:open={['/pages', '/helpcenter', '/blog', '/authpages', '/utility','/special'].includes(openMenu)} class="submenu">
                            <li class:active={activeIndex === '/aboutus'}>
                                <Link to="/aboutus" class="sub-menu-item"
                                    >About Us</Link
                                >
                            </li>
                            <li class:active={activeIndex === '/services'} >
                                <Link to="/services" class="sub-menu-item"
                                    >Services</Link
                                >
                            </li>
                            <li class:active={activeIndex === '/pricing'}>
                                <Link to="/pricing" class="sub-menu-item"
                                    >Pricing
                            </Link>
                            </li>

                            <li class:active={['/heplcenter', '/helpcenter-overview', '/helpcenter-faqs', '/helpcenter-guides', '/helpcenter-support'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#helpcenter" on:click={() => submenu(openMenu === '/heplcenter' ? '' : '/helpcenter')}> Helpcenter </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/helpcenter'} class="submenu">
                                    <li class:active={activeIndex === '/helpcenter-overview'}>
                                        <Link
                                            to="/helpcenter-overview"
                                            class="sub-menu-item">Overview</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/helpcenter-faqs'}>
                                        <Link
                                            to="/helpcenter-faqs"
                                            class="sub-menu-item">FAQs</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/helpcenter-guides'}>
                                        <Link
                                            to="/helpcenter-guides"
                                            class="sub-menu-item">Guides</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/helpcenter-support'}>
                                        <Link
                                            to="/helpcenter-support"
                                            class="sub-menu-item">Support</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={['/blog', '/blogs', '/blog-sidebar', '/blog-detail'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#blog" on:click={() => submenu(openMenu === '/blog' ? '' : '/blog')}> Blog </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/blog'} class="submenu">
                                    <li class:active={activeIndex === '/blogs'}>
                                        <Link
                                            to="/blogs"
                                            class="sub-menu-item"
                                        >
                                            Blogs</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/blog-sidebar'}>
                                        <Link
                                            to="/blog-sidebar"
                                            class="sub-menu-item"
                                        >
                                            Blog Sidebar</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/blog-detail'}>
                                        <Link
                                            to="/blog-detail"
                                            class="sub-menu-item"
                                        >
                                            Blog Detail</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={['/authpages', '/login', '/signup', '/reset-password', '/lock-screen'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#authpages" on:click={() => submenu(openMenu === '/authpages' ? '' : '/authpages')}> Auth Pages </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/authpages'} class="submenu">
                                    <li class:active={activeIndex === '/login'}>
                                        <Link
                                            to="/login"
                                            class="sub-menu-item"
                                        >
                                            Login</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/signup'}>
                                        <Link
                                            to="/signup"
                                            class="sub-menu-item"
                                        >
                                            Signup</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/reset-password'}>
                                        <Link
                                            to="/reset-password"
                                            class="sub-menu-item"
                                        >
                                            Forgot Password</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/lock-screen'}>
                                        <Link
                                            to="/lock-screen"
                                            class="sub-menu-item"
                                        >
                                            Lock Screen</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={['/utility', '/terms', '/privacy'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#utility" on:click={() => submenu(openMenu === '/utility' ? '' : '/utility')}> Utility </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/utility'} class="submenu">
                                    <li class:active={activeIndex === '/terms'}>
                                        <Link
                                            to="/terms"
                                            class="sub-menu-item"
                                            >Terms of Services</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/privacy'}>
                                        <Link
                                            to="/privacy"
                                            class="sub-menu-item"
                                            >Privacy Policy</Link
                                        >
                                    </li>
                                </ul>
                            </li>

                            <li class:active={['/comingsoon', '/maintenance', '/error'].includes(activeIndex)} class="has-submenu parent-menu-item">
                                <a href="#special" on:click={() => submenu(openMenu === '/special' ? '' : '/special')}> Special </a><span
                                    class="submenu-arrow"
                                ></span>
                                <ul class:open={openMenu === '/special'} class="submenu">
                                    <li class:active={activeIndex === '/comingsoon'}>
                                        <Link
                                            to="/comingsoon"
                                            class="sub-menu-item"
                                        >
                                            Coming Soon</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/maintenance'}>
                                        <Link
                                            to="/maintenance"
                                            class="sub-menu-item"
                                        >
                                            Maintenance</Link
                                        >
                                    </li>
                                    <li class:active={activeIndex === '/error'}>
                                        <Link
                                            to="/error"
                                            class="sub-menu-item"
                                        >
                                            404! Error</Link
                                        >
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </li>

                    <li class:active={activeIndex === '/contactus'}>
                        <Link to="/contactus" class="sub-menu-item"
                            >Contact Us</Link
                        >
                    </li>
                </ul>
                <!--end navigation menu-->
            </div>
            <!--end navigation-->
        </div>
    </header>
</main>

<style>
</style>
