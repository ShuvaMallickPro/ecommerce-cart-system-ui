<template>
  <div class="col bg-white border border-slate-200 rounded-2xl shadow-md">
    <div
      class="h-60 max-h-60 overflow-hidden justify-center items-center px-16 py-2 content-center"
    >
      <img
        class="w-36 mx-auto py-3"
        :src="product.image"
        :alt="product.title"
        @error="handleImgError"
      />
    </div>

    <div class="card-body py-4 px-5">
      <h2 class="font font-bold text-lg text-slate-600 mb-1 truncate">
        {{ product.title }}
      </h2>
      <p class="font font-regular text-slate-500 mb-4 truncate">
        {{ product.description }}
      </p>
      <div class="flex justify-between items-center">
        <p class="font font-bold text-xl text-slate-600">
          ${{ product.price }}
        </p>
        <button
          class="bg-primary py-2 px-4 rounded-full text-slate-200 font-medium hover:bg-primaryDark transition300 whitespace-nowrap"
          @click="handleAddToCart(product.id)"
        >
          Add to Cart
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions } from "pinia";
import { useCartStore } from "../store/cartsStore";
import { PLACEHOLDER_PRODUCT_IMAGE_URL } from "../utils/images";

export default {
  props: {
    product: {
      type: Object,
      default: {},
      required: true,
    },
  },

  methods: {
    ...mapActions(useCartStore, ["handleAddToCart"]),
    handleImgError(e) {
      if (e?.target?.src !== PLACEHOLDER_PRODUCT_IMAGE_URL) {
        e.target.src = PLACEHOLDER_PRODUCT_IMAGE_URL;
      }
    },
  },
};
</script>
