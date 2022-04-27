<script>

    export let double;

    $: state = 0;

    function changeState() {
        if (state == 0)
            state++;
        else
            state--;
        window.update();
    }

</script>

<div class="hole">
    <div class="demo">
        <i class="fas fa-arrow-left" id="left" on:click={changeState}></i>
            {#if double}
                {#if state == 0}
                    <video muted width="300" controls="controls">
                        <source src="/assets/demos/double1.mp4" type="video/mp4">
                    </video>
                {:else}
                    <video muted width="300" controls="controls">
                        <source src="/assets/demos/double2.mp4" type="video/mp4">
                    </video>
                {/if}
            {:else}
                {#if state == 0}
                    <video muted width="300" controls="controls">
                        <source src="/assets/demos/crash1.mp4" type="video/mp4">
                    </video>
                {:else}
                    <video muted width="300" controls="controls">
                        <source src="/assets/demos/crash2.mp4" type="video/mp4">
                    </video>
                {/if}
            {/if}
        <i class="fas fa-arrow-right" id="right" on:click={changeState}></i>
    </div>
</div>

<style>

    video {
        box-shadow: 0 5px 10px 0 rgba(0, 0, 0, 0.2), 0 8px 20px 0 rgba(0, 0, 0, 0.19);
    }

    #left {
        transition: .5s;
        transform: translateX(0);
    }

    #left:hover {
        transition: .5s;
        transform: translateX(-.3em);
    }

    #right {
        transition: .5s;
        transform: translateX(0);
    }

    #right:hover {
        transition: .5s;
        transform: translateX(.3em);
    }

    .hole {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        margin-right: -10%;
        margin-left: -10%;
    }

    .demo {
        display: flex;
        justify-content: space-around;
        align-items: center;
        transition: 1s;
    }

    .demo i {
        color: white;
        font-size: 1.2rem;
        margin: 1rem;
        cursor: pointer;
    }
    
</style>