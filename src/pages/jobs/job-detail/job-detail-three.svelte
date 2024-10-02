<script>
    import Navbar from "../../../components/navbar.svelte";
    import Threedetail from "../../../components/job-detail/detail-three.svelte";
    import Related from "../../../components/job-detail/related-three.svelte";
    import Footers from "../../../components/footer/footer.svelte";
    import Backtotop from "../../../components/back-to-top.svelte";
</script>

<main>
    <Navbar logoDark={true} />

    <section class="bg-half d-table w-100">
        <Threedetail />
        <div class="container mt-100 mt-60">
            <Related />
        </div>
    </section>
    <Footers explore={true} footerbar={'footer-bar'} />
    <Backtotop />
</main>

<style lang="scss" scoped></style>
