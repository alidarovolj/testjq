<template>
    <div class="container">
        <h1 class="text-3xl my-3 text-center font-bold">TicTacToe</h1>
        <div class="flex flex-wrap w-2/3 mx-auto">
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl border-r-4 border-l-4 border-black">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl">
                &nbsp;
            </div>

            <div class="slot py-4 font-bold text-center w-1/3 text-3xl border-t-4 border-b-4 border-black">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl border-4 border-black">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl border-t-4 border-b-4 border-black">
                &nbsp;
            </div>

            <div class="slot py-4 font-bold text-center w-1/3 text-3xl">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl border-r-4 border-l-4 border-black">
                &nbsp;
            </div>
            <div class="slot py-4 font-bold text-center w-1/3 text-3xl">
                &nbsp;
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TicTacToe",
    mounted() {
        console.log('hjdksa');
    }
}
</script>