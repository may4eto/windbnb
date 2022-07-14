<script>
    const toggleHeader = function() {
        const pixels = window.pageYOffset
        if (pixels > 10) {
            document.querySelector('header').classList.add('scrolled')
        } else {
            document.querySelector('header').classList.remove('scrolled')
        }
    }
    document.addEventListener('scroll', function() {
        toggleHeader()
    })
</script>

<header>
    <div class="wrapper">
        <img src="images/logo.svg" alt="Windbnb logo" />
        <div class="search">
            <input type="text" placeholder="Search location"/>
            <button>
                <span class="material-symbols-rounded">
                search
                </span>
            </button>
        </div>
    </div>
</header>

<style>
    header {
        background-color: var(--white);
        padding: 1.5rem 0;
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
    }
    header .wrapper {
        width: 80vw;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    header .search {
        position: relative;
    }
    header .search input {
        border-radius: 1rem;
        height: 2rem;
        border: none;
        -webkit-box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
        box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
        padding: 0 1rem;
        max-width: 25vw;
    }
    header .search button {
        appearance: none;
        border: none;
        background-color: transparent;
        position: absolute;
        right: 0.5rem;
        top: 0.2rem;
        cursor: pointer;
    }
    header .search button span {
        color: var(--middle-grey);
    }
    :global(header.scrolled) {
        -webkit-box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
        box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
    }
</style>