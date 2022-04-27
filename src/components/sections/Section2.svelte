<script>

    import Vantagens from '../cards/Vantagens.svelte';
    import VideoDemos from '../cards/VideoDemos.svelte';

    function openTikTok() {
        window.open('https://www.tiktok.com/@vemganharmoney', '_blank').blur();
    }

</script>

<section>
    <h1>VANTAGENS</h1>
    <hr>
    <div class="vantagens">
        <Vantagens icon='<i class="fas fa-network-wired"></i>' text="Qualquer plataforma"/>
        <Vantagens icon='<i class="fas fa-street-view"></i>' text="Qualquer lugar"/>
        <Vantagens icon='<i class="far fa-clock"></i>' text="Otimização do seu tempo"/>
        <Vantagens icon='<i class="fas fa-wrench"></i>' text="Atualizações diárias"/>
    </div>
    <h1>DEMONSTRAÇÕES</h1>
    <hr id="demo">
    <div class="demos">
        <VideoDemos double={true} />
        <VideoDemos double={false} />
    </div>
    <p>Disponibilizamos mais demonstrações em nosso <span on:click={openTikTok}>TikTok</span></p>
</section>

<style>

    section {
        text-align: center;
        padding-top: 1rem;
    }

    h1 {
        font-weight: 700;
        font-size: 40px;
        color: white;
    }

    p {
        color: white;
        font-size: 18px;
        font-weight: 600;
    }

    span {
        color: #2f9f60;
        cursor: pointer;
        text-decoration: underline;
    }

    hr {
        width: 24%;
    }

    #demo {
        width: 35%;
    }

    .vantagens {
        display: flex;
        justify-content: space-evenly;
        padding: 5rem;
    }

    .demos {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        padding: 5rem;
    }

    @media only screen and (max-width: 1138px) {
        .demos {
            display: flex;
            flex-direction: column;
            justify-content: space-evenly;
            align-items: center;
            gap: 2rem;
            padding: 3rem;
        }
        .vantagens {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 2rem;
            padding: 5rem;
        }
        hr {
            width: 18rem;
        }
        #demo {
            width: 20rem;
        }
    }

</style>