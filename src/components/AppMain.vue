<script>

export default {
    name: 'AppMain',
    data: ()=>({
        mainText: 'Content goes here'
    })
}
</script>

<template>
    <main>
        <div class="container">
            <p>{{mainText}}</p>
        </div>
        
    </main>
</template>

<style lang="scss">
main {
    background-color: #000000;
    padding: 32px 0;
    color: #ffffff;

    p{
        font-size: 24px;
    }

}
</style>
