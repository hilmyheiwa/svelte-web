<script>
    import Navbar from '../../components/navbar.svelte';
    import imageSrc from '../../assets/images/team/01.jpg';
    import imageSrcTwo from '../../assets/images/hero/bg5.jpg';
    import Setting from '../../components/candidates/candidate-profile-setting.svelte';
    import Footers from '../../components/footer/footer.svelte';
    import Backtotop from '../../components/back-to-top.svelte'
    
    let ImageSrc = (imageSrc)
    let image = ('')
    let ImageSrcTwo = (imageSrcTwo)
    let imageTwo = ('')
    
    let loadFile = (event) => {
       image = document.getElementById(event.target.name);
       ImageSrc = URL.createObjectURL(event.target.files[0]);
    }
    
    let loadFileTwo = (event) => {
       imageTwo = document.getElementById(event.target.name);
       ImageSrcTwo = URL.createObjectURL(event.target.files[0]);
    }
    
    </script>

<main>
    <Navbar logoDark={true} />
    <section class="section">
       <div class="container">
          <div class="row">
             <div class="col-12">
                <div class="position-relative">
                   <div class="candidate-cover">
                      <div class="profile-banner relative text-transparent">
                         <input id="pro-banner" name="profile-banner" type="file" class="hidden" on:change={loadFileTwo} />
                         <div class="relative shrink-0">
                            <img src={ImageSrcTwo} class="rounded shadow" id="profile-banner" alt="">
                            <label class="profile-image-label" for="pro-banner"></label>
                         </div>
                      </div>
                   </div>
                   <div class="candidate-profile d-flex align-items-end mx-2">
                      <div class="profile-pic">
                         <input id="pro-img" name="profile-image" type="file" class="d-none" on:change={loadFile} />
                         <div class="position-relative d-inline-block">
                            <img src={ImageSrc} class="avatar avatar-medium img-thumbnail rounded-pill shadow-sm"
                               id="profile-image" alt="">
                            <label class="icons position-absolute bottom-0 end-0" for="pro-img"><span
                                  class="btn btn-icon btn-sm btn-pills btn-primary"><i data-feather="camera"
                                     class="icons"></i></span></label>
                         </div>
                      </div>
 
                      <div class="ms-2">
                         <h5 class="mb-0">Mr. Calvin Carlo</h5>
                         <p class="text-muted mb-0">Web Designer</p>
                      </div>
                   </div>
                </div>
             </div><!--end col-->
          </div><!--end row-->
       </div><!--end container-->
 
       <div class="container">
          <Setting />
       </div>
    </section>
    <Footers explore={true} footerbar={'footer-bar'} />
    <Backtotop />
 </main>
  
 <style lang="scss" scoped></style>