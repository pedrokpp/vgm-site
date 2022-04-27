<script>
    
    import Card from '../cards/Card.svelte';
    import Divider from '../dividers/Divider.svelte'

</script>

<div class="content">
    <section>
        <img class="logo" src="/assets/vgmlogo.png" alt="logo">
        <h1>O robô de apostas mais preciso do Brasil</h1>
        <div class="planos">
            <Card title="DOUBLE" subtitle="🟥⬜⬛" sinais="150"/>
            <Card title="GRATUITO" subtitle='<i class="fas fa-coins"></i>' btnmsg="ENTRE AGORA" sinais="40" isSinal={false}/>
            <Card title="CRASH" subtitle='<i class="fas fa-meteor"></i>' sinais="120"/>
        </div>
        <img class="garantia" height="155rem" src="./assets/garantia-de-7-dias-1.png" alt="Garantia até 7 dias 100% do dinheiro de volta">
        <Divider />
    </section>
</div>

<style>

    @keyframes stretch {
        0% {
            transform: scale(1.1);
        }
  
        100% {
            transform: scale(1.25);
        }
    }

    .garantia {
        animation-name: stretch;
        animation-duration: 2.0s;
        animation-timing-function: ease-out;
        animation-direction: alternate;
        animation-iteration-count: infinite;
        animation-play-state: running;    
    }

    section {
        text-align: center;
        background-color: rgba(255, 255, 255, 0.35);
        color: var(--main-blue);
        padding-bottom: 1rem;
        display: block;
    }

    .content {
        background: url('/assets/roulette.jpg');
    }

    .logo {
        width: auto;
        height: 14rem;
    }

    h1 {
        text-decoration: underline;
        font-size: xx-large;
    }

    .planos {
        display: flex;
        justify-content: space-evenly;
        padding-top: 1.2rem;
        padding-bottom: 1.2rem;
    }

    @media only screen and (max-width: 1138px) {
        .planos {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
            padding: 1.2rem;
        }
        .logo {
            width: 20rem;
            height: auto;
        }
        h1 {
            font-size: x-large;
        }
    }

</style>