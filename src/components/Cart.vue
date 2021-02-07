<template>
<div>
    <h2>Books in Cart</h2>
    <div v-bind:key="book.bookid" v-for="book in cart">
        <CartItem v-bind:book="book" />
    </div>
</div>
</template>

<script>
import CartItem from './CartItem.vue';
export default {
    name: "Cart",
    props: ["cart"],
    components: {
        CartItem
    },

}
</script>

<style scoped>
.book-item {
    background: #e6f2ff;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
}
</style>
