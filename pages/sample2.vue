<template lang="pug">
  div
    | {{$store.state.counter}}
    | {{$store.state.var1}}
    | {{$store.state.submod.var2}}

</template>

<script>

import Vuex from "vuex"

const store = new Vuex.Store({
  state: () => ({
    var1: 1,
  }),
  modules: {
    submod: {
      namespaced: true,
      state: () => ({
        var2: 2,
      }),
    },
  }
})

import { mapMutations } from 'vuex'

export default {
  store,
}
</script>
