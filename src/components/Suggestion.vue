<template>
        <div class="second">
            <div class="pp">
                    <q-icon name="person" class="side-img" />
                    <p>Lorem Dude <br> <span>Lorem ipsum and vibes</span></p>
            </div>
            <p class="blue-text">Follow</p>
        </div>
</template>

<script>
export default {
    name: 'Suggestion',
}
</script>

<style scoped>
    p{
        font-size: 0.75rem;
    }

    .second{
        display: flex;
        justify-content: space-between;
        margin: 3% 0;
    }

     .side-profile{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 20px;
    }

    .side-img{
        border: 1px solid;
        border-radius: 50%;
        width: 30px;
        height: 30px;
        font-size: 1.5rem;
        margin: auto 0;
    }

    .pp{
        display: flex;

    }

    .pp p{
        margin: auto 0;
        margin-left: 7px;
    }
    .blue-text{
        color: blue;
        margin: auto 0;
    }
</style>