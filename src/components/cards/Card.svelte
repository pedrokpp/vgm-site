<script>

    export let title;
    export let subtitle;
    export let sinais;
    export let btnmsg = "ASSINE AGORA";
    export let isSinal = true;

    function openLink() {
        if (title == "DOUBLE") {
            window.open('https://lastlink.com/p/CCEDABE0A', '_blank');
        } else if (title == "CRASH") {
            window.open('https://lastlink.com/p/C038CCA97', '_blank');
        } else {
            window.open('https://t.me/vemganharmoney', '_blank');
        }
    }

</script>

<div class="container">
    
    <h1>{title}</h1>
    <h2>{@html subtitle}</h2>
    <hr> <br>
    <div class="info">
        {#if isSinal}
            <span><i class="fas fa-user-check"></i>  {sinais} <span style="color: #89ff45;">GREENS</span> diários!</span>
        {:else}
            <span><i class="fas fa-user-check"></i>  Teste os sinais <span style="color: yellow;">gratuitamente</span>!</span>
        {/if}
        <br>
        <span><i class="fas fa-user-check"></i>  Suporte <span style="color: yellow;">dedicado</span>!</span>
        <br>
        <span><i class="fas fa-user-check"></i>  <span style="color: yellow;">Baixo</span> investimento incial!</span>
        <br>
        {#if isSinal}
            <span><i class="fas fa-user-check"></i>  <span style="color: yellow;">24 horas</span> de sinais por dia!</span>
        {:else}
            <span><i class="fas fa-user-check"></i>  <span style="color: yellow;">1 hora</span> de sinais por dia!</span>
        {/if}
        <br>
        <span><i class="fas fa-user-check"></i>  Conteúdos explicativos!</span>
        <br>
        <span><i class="fas fa-user-check"></i>  Sem necessidade de experiência!</span>
        <button on:click={openLink}><strong>{btnmsg}</strong></button>
    </div>

</div>

<style>

    hr {
        width: 80%;
    }

    .container {
        color: white;
        width: 350px;
        height: 500px;
        background-color: #03223e;
        border-radius: 5%;
        box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 8px 20px 0 rgba(0, 0, 0, 0.19);
        z-index: 3;
        transition: 1s;
        transform: translateY(0);
    }

    .container:hover {
        transition: 1s;
        transform: translateY(-1rem);
    }

    .info {
        font-weight: 300;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }

    button {
        width: 65%;
        cursor: pointer;
        user-select: auto;
        margin-top: 3.5rem;
        padding: 0.8rem;
        font-weight: 700;
    }

</style>