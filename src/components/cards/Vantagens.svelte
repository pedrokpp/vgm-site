<script>

    export let icon;
    export let text

</script>

<div class="main">
    <span class="ic">{@html icon}</span>
    <span class="txt">{text}</span>
</div>

<style>

    .main {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

    .ic {
        color: #2f9f60;
        font-size: 40px;
    }

    .txt {
        font-size: 24px;
        font-weight: 500;
        color: rgb(202, 202, 202);
    }

</style>