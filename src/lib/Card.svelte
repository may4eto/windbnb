<script>
    export let item
</script>
<div class="card">
    <img src="{item.photo}" alt="" />
    <div class="info">
        <p>
            {#if item.superHost}
            <span class="superhost">superhost</span>
            {/if}
            <span>{item.type}</span>
            {#if item.beds}
            <span> . {item.beds} beds</span>
            {/if}
        </p>
            <div class="rating">
                <span class="star material-symbols-rounded">star</span>
                <span>{item.rating}</span>
            </div>
    </div>
    <h3>{item.title}</h3>
</div>

<style>
    .card img {
        display: block;
        width: 100%;
        height: auto;
        object-fit: cover;
        aspect-ratio: 3/2;
        border-radius: 1.5rem;
    }
    .card .info {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .card .info p {
        color: var(--middle-grey);
        font-size: 0.875rem;
    }
    .card .info p span.superhost {
        color: var(--dark-grey);
        text-transform: uppercase;
        padding: 0.25rem 0.5rem;
        border: solid 1px var(--dark-grey);
        border-radius: 0.75rem;
        margin-right: 0.5rem;
        font-size: 0.75rem;
    }
    .rating {
        display: flex;
        align-items: center;
    }
    .rating span {
        color: var(--dark-grey);
    }
    .rating span.star {
        color: var(--accent);
        font-size: 1rem;
    }
    .card h3 {
        margin-top: 0;
        font-weight: 600;
    }
</style>