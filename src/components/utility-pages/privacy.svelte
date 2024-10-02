<script>

    const datas = ['It seems that only fragments of the original text remain in the Lorem Ipsum texts used today. One may speculate that over the course of time certain letters were added or deleted at various positions within the text.', 'In the 1960s, the text suddenly became known beyond the professional circle of typesetters and layout designers when it was used for Letraset sheets (adhesive letters on transparent film, popular until the 1980s) Versions of the text were subsequently included in DTP programmes such as PageMaker etc.', 'There is now an abundance of readable dummy texts. These are usually used  when a text is required purely to fill a space. These alternatives to the classic Lorem Ipsum texts are often amusing and tell short, funny or nonsensical stories.', 'Digital Marketing Solutions for Tomorrow', 'Our Talented & Experienced Marketing Agency', 'Create your own skin to match your brand', 'Digital Marketing Solutions for Tomorrow', 'Our Talented & Experienced Marketing Agency', 'Create your own skin to match your brand']
    
    </script>

<main>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-9">
                <div class="card shadow rounded border-0">
                    <div class="card-body">
                        <h5 class="card-title">Overview :</h5>
                        {#each datas.slice(0, 3) as item }
                        <p class="text-muted">{ item }</p>                            
                        {/each}

                        <h5 class="card-title">We use your information to :</h5>
                        <ul class="list-unstyled text-muted mt-3">
                            {#each datas.slice(3, 9) as item}
                            <li class="mt-2"><i data-feather="arrow-right"
                                    class="fea icon-sm me-2"></i>{ item }</li>
                            {/each}
                        </ul>

                        <h5 class="card-title mt-3">Information Provided Voluntarily :</h5>
                        <p class="text-muted">In the 1960s, the text suddenly became known beyond the professional
                            circle of typesetters and layout designers when it was used for Letraset sheets (adhesive
                            letters on transparent film, popular until the 1980s) Versions of the text were subsequently
                            included in DTP programmes such as PageMaker etc.</p>

                        <a href="#name" class="btn btn-primary">Print</a>
                    </div>
                </div>
            </div><!--end col-->
        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>