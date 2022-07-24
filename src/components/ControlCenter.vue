<template>
  <button @click="inc">Increment</button>
</template>

<script>
import { useStore } from 'vuex';
export default {
  setup() {
    const store = useStore();
    //we got access to the store by using the useStore() function inside the store();
    //
    function inc() {
      store.dispatch('increment');
    }

    return { inc };
  },
};
</script>