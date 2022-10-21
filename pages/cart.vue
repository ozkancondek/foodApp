<template>
  <main v-if="productCount > 0" class="cart container">
    <h2>Your Cart</h2>

    <section>
      <table>
        <thead>
          <tr>
            <th>Item</th>
            <th>Add Ons</th>
            <th>Amount</th>
            <th>Total Price</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in cart" :key="item.id">
            <td>
              {{ item.item }}
              <span v-if="item.options">- {{ item.options }}</span>
            </td>
            <td>
              <span v-for="addon in item.addOns" :key="addon" class="comma">{{
                addon
              }}</span>
            </td>
            <td>{{ item.count }}</td>
            <td>{{ item.combinedPrice }}</td>
          </tr>
          <tr>
            <td colspan="3"></td>
            <td class="total">Total:{{ totalPrice.toFixed(2) }}</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>
  <p v-else>No product</p>
</template>

<script>
import { mapGetters, mapState } from "vuex";

export default {
  computed: {
    ...mapGetters(["totalPrice", "productCount"]),
    ...mapState(["cart"]),
  },
};
</script>

<style lang="scss" scoped></style>
