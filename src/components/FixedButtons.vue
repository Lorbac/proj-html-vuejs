<template>
    <div>
        <div class="sticky-top-button">
            <i class="fas fa-folder-open"></i>
            <p>Demos</p>
        </div>
        <div class="sticky-bottom-button">
            <span class="dollar">$</span><span>39</span>
            <p>On Sale</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "FixedButtons"
}
</script>

<style lang="scss" scoped>

    @import '../styles/vars.scss';

    .sticky-top-button, .sticky-bottom-button {
        width: 65px;
        height: 65px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        position: fixed;
        z-index: 999;
        background-color: $white;
        border-radius: 10px;
        cursor: pointer;
        box-shadow: 0px 0px 46px -9px rgba(0,0,0,0.7);

        .fas {
          color: $tundora;
          font-size: 25px;
        }

        p {
          color: $tundora;
          font-size: 12px;
        }
    }

    .sticky-top-button {
        right: 20px;
        top: 150px;
    }

    .sticky-bottom-button {
        right: 20px;
        top: 225px;

        .dollar {
            position: absolute;
            left: 12px;
            top: 11px;
            font-size: 12px;
        }

        span {
            font-size: 25px;
            color: $keppel;
        }
    }
</style>