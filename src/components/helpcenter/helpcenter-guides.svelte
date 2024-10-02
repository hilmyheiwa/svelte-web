<script>
    
    const guidesData = [
        {
            title: 'Getting started',
            features: [
                'Deciding to purchase', 'List your space', 'Landing an experience or adventure', 'Top uses questions'
            ]
        },
        {
            title: 'Your calendar',
            features: [
                'Pricing & availability', 'Booking settings', 'Responding to enquiries & requests', 'Snoozing or deactivating your listing'
            ],
            class: ' mt-4 mt-sm-0 pt-2 pt-sm-0'
        },
        {
            title: 'Your listings',
            features: [
                'Updating your listing', 'Neighbourhoods', 'Listing photos & photography', 'Travosy Plus', 'API-connected software'
            ],
            class: 'mt-4 mt-lg-0 pt-2 pt-lg-0 pt-2'
        },
        {
            title: 'How payouts work',
            features: [
                'Getting paid', 'Adding payout info', 'Your payout status', 'Donations', 'Taxes'
            ],
            class: 'mt-4 pt-2'
        },
        {
            title: 'Your reservations',
            features: [
                'Travosy safely', 'Travosy Experiences and Adventures', 'Changing a reservation', 'Cancelling a reservation', 'Long-term reservations'
            ],
            class: 'mt-4 pt-2'
        },
        {
            title: 'Reservation help',
            features: [
                'Help with a reservation or guest', 'Guest cancellations'
            ],
            class: ' mt-4 pt-2'
        },
        {
            title: 'Your account',
            features: [
                'Your profile', 'Account security', 'Identification & verifications', 'Reviews', 'Superhost status'
            ],
            class: 'mt-4 pt-2'
        }
    ]
    </script>

<main>
    <div class="container">
        <div class="row">
            {#each guidesData as item}
            <div class={`col-lg-4 col-md-6 col-12 ${item.class}`}>
                <h5>{ item.title }</h5>
                <ul class="list-unstyled mt-4 mb-0">
                    {#each item.features as features}
                    <li class="mt-2"><a href="#name" class="text-muted"><i
                                class="mdi mdi-arrow-right text-primary me-2"></i>{ features }</a></li>
                    {/each}
                </ul>
            </div><!--end col--> 
            {/each}
           
        </div><!--end row-->
    </div><!--end container-->
</main>

<style lang="scss" scoped></style>