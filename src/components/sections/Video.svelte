<script>
    import { onMount } from "svelte";


    let showModal = true;

    let vid;

    onMount(() => {
        setTimeout(() => vid.play(), 1000);
    });

    function triggerModal() {
        showModal = !showModal;
    }

    function openIG() {
        window.open('https://instagram.com/vemganharmoney', '_blank');
    }

    function openYT() {
        window.open('https://www.youtube.com/channel/UCiqGMKztNkkFl_zKBNZRadg', '_blank');
    }

    function openTT() {
        window.open('https://www.tiktok.com/@vemganharmoney', '_blank');
    }

</script>

<div class="modal">
    <div class="socials">
        <div class="side-right">
            <i on:click="{openYT}" class="circle fab fa-youtube"></i>
            <i on:click="{openTT}" class="circle fab fa-tiktok"></i>
        </div>
        <div class="side-left">
            <i on:click="{openIG}" class="circle fab fa-instagram"></i>
            <i on:click="{triggerModal}" style="font-size: 1.5rem;" class="circle fas fa-desktop"></i>
        </div>
    </div>
    {#if showModal}
        <div class="bg">
            <div class="videoframe">
                <svg on:click="{triggerModal}" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--! Font Awesome Pro 6.0.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M310.6 361.4c12.5 12.5 12.5 32.75 0 45.25C304.4 412.9 296.2 416 288 416s-16.38-3.125-22.62-9.375L160 301.3L54.63 406.6C48.38 412.9 40.19 416 32 416S15.63 412.9 9.375 406.6c-12.5-12.5-12.5-32.75 0-45.25l105.4-105.4L9.375 150.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L160 210.8l105.4-105.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-105.4 105.4L310.6 361.4z"/></svg>
                <div class="organizer">
                    <video bind:this={vid} width="60%" height="300" autoplay loop controls='controls'>
                        <source src='./vsl.mp4'>
                        <track src="./captions.vtt" kind="captions" srclang="pt-br" label="legenda">
                    </video>
                    <p>ASSISTA ESSE VÍDEO ANTES DE COMPRAR</p>
                    <p id="reminder">*93% das pessoas não assistem o vídeo até o final</p>
                </div>
            </div>
        </div>
    {/if}
</div>

<style>

    .circle {
        background-color: #2f9f60;
        color: black;
        border: .125rem solid black;
        font-size: 2rem;
        width: 3rem;
        height: 3rem;
        border-radius: 50%;
        box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 8px 20px 0 rgba(0, 0, 0, 0.19);
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
    }

    .socials {
        display: flex;
        justify-content: space-between;
    }

    .side-right {
        top: 50%;
        right: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        padding-right: 1rem;
        position: fixed;
        z-index: 4;
    }

    .side-left {
        top: 50%;
        left: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        padding-left: 1rem;
        position: fixed;
        z-index: 4;
    }

    .bg {
        position: fixed;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.8);
        z-index: 4;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .videoframe {
        position: relative;
        border-radius: 5px;
        background-color: var(--main-blue);
        box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 8px 20px 0 rgba(0, 0, 0, 0.19);
        width: 60rem;
        height: 32rem;
        border: .0125rem solid white;
    }

    .videoframe svg {
        position: absolute;
        top: 0;
        right: 0;
        margin: .5rem;
        height: 1rem;
        width: auto;
        fill: white;
    }

    .videoframe p {
        color: white;
        font-weight: 600;
    }

    .organizer {
        padding-top: 5rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: .3rem;
    }

    #reminder {
        font-size: 12px;
        font-weight: 300;
    }

    @media only screen and (max-width: 1138px) {
        .organizer {
            padding-top: .8rem;
            gap: 0;
        }
        video {
            width: 70%;
            height: 75%;
        }
        .videoframe {
            width: 90rem;
            height: 18rem;
        }

    }

</style>