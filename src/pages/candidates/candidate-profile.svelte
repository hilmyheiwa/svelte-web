<script>
    import { Link } from 'svelte-routing';
    import profile from '../../assets/images/team/01.jpg';
    import Navbar from '../../components/navbar.svelte';
    import CandidateInfo from '../../components/candidates/candidate-info.svelte';
    import Related from '../../components/candidates/candidate-related.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte';
    import heroimg from '../../assets/images/hero/bg5.jpg'
    </script>

<main>
    <Navbar logoDark={true} />
    <section class="section">
       <div class="container">
          <div class="row">
             <div class="col-12">
                <div class="position-relative">
                   <div class="candidate-cover">
                      <img src={heroimg} class="img-fluid rounded shadow" alt="">
                   </div>
                   <div class="candidate-profile d-flex align-items-end justify-content-between mx-2">
                      <div class="d-flex align-items-end">
                         <img src={profile}
                            class="rounded-pill shadow border border-3 avatar avatar-medium" alt="">
 
                         <div class="ms-2">
                            <h5 class="mb-0">Mr. Calvin Carlo</h5>
                            <p class="text-muted mb-0">Web Designer</p>
                         </div>
                      </div>
 
                      <Link to="/candidate-profile-setting"
                         class="btn btn-sm btn-icon btn-pills btn-soft-primary"><i data-feather="settings"
                            class="icons"></i></Link>
                   </div>
                </div>
             </div><!--end col-->
          </div><!--end row-->
       </div><!--end container-->
 
       <CandidateInfo />
 
       <div class="container mt-100 mt-60">
          <Related />
       </div>
    </section>
    <Footers explore={true} footerbar={'footer-bar'} />
    <Backtotop />
 </main>
 
 
 <style lang="scss" scoped></style>