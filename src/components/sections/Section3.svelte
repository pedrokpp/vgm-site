<script>

    let numeros = [1, 2, 3, 4, 5, 6]

    function openInstagram() {
        window.open('https://www.instagram.com/vemganharmoney/', '_blank');
    }

</script>

<section>
    <h1>OPINIÕES DOS CLIENTES</h1>
    <hr>
    <div class="feedbacks">
        {#each numeros as numero}
            <img class="feedback" width="300" src="/assets/feedbacks/{numero}.jpg" alt={numero}>
        {/each}
        <p>Veja mais em nosso <span on:click={openInstagram}>Instagram</span></p>
    </div>
</section>

<style>

    section {
        background-color: #2f9f60;
        text-align: center;
        padding-top: 3rem;
    }

    img {
        box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 8px 20px 0 rgba(0, 0, 0, 0.19);
    }

    span {
        color: white;
    }
    
    h1 {
        font-weight: 700;
        font-size: 40px;
        color: var(--main-blue);
    }

    hr {
        width: 24%;
        border: none;
        height: 2px;
        background-color: var(--main-blue);
    }

    .feedbacks {
        padding: 3rem;
        display: grid;
        grid-template-columns: auto auto auto;
        justify-content: space-around;
        align-content: center;
        row-gap: 1.2rem;
    }

    .feedbacks p {
        padding-top: 2rem;
        grid-column: 2;
        font-size: 18px;
        font-weight: 600;
    }

    .feedbacks span {
        cursor: pointer;
        text-decoration: underline;
    }

    @media only screen and (max-width: 1138px) {
        .feedbacks {
            padding: 3rem;
            display: flex;
            flex-direction: column;
            justify-content: space-evenly;
            align-items: center;
            gap: 2rem;
            row-gap: 1.2rem;
        }

        .feedbacks p {
            padding-top: 2rem;
            font-size: 18px;
            font-weight: 600;
        }

        .feedbacks span {
            cursor: pointer;
            text-decoration: underline;
        }
    }

</style>