<script>
    import Sidebar from "../../components/job-sidebar.svelte";
    import Pagination from "../../components/pagination.svelte";
    import Joblist from '../../components/job-list/list-one.svelte';
</script>

<div class="container">
    <div class="row g-4">
        <Sidebar />

        <div class="col-lg-8 col-md-6 col-12">
            <Joblist width={'w-250px'} />

            <Pagination />
        </div>
    </div>
</div>

<!--end container-->

<style lang="scss" scoped></style>
