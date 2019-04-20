<template>
  <div>
    <div class="container">
      <ul class="tabsul">
        <div class="d-flex" :class="{ divdisplaynone: currentTab !== 1 }">
          <li
            @click="selectTab(1)"
            class="tabstitle newclass"
            :class="{ newclass2: currentTab == 1 }"
          >
            Datos personales
          </li>
          <button @click="nexttab(2)">next</button>
        </div>
        <div class="d-flex" :class="{ divdisplaynone: currentTab !== 2 }">
          <li
            @click="selectTab(2)"
            class="tabstitle newclass"
            :class="{ newclass2: currentTab == 2 }"
          >
            Informacion personal
          </li>
          <button @click="nexttab(3)">next</button>
        </div>
        <div class="d-flex" :class="{ divdisplaynone: currentTab !== 3 }">
          <li
            @click="selectTab(3)"
            class="tabstitle newclass"
            :class="{ newclass2: currentTab == 3 }"
          >
            Verificación
          </li>
          <button @click="nexttab(4)">next</button>
        </div>
        <div class="d-flex" :class="{ divdisplaynone: currentTab !== 4 }">
          <li
            @click="selectTab(4)"
            class="tabstitle newclass"
            :class="{ newclass2: currentTab == 4 }"
          >
            Obteniendo tu avance
          </li>
          <button @click="nexttab(5)">next</button>
        </div>
        <div class="d-flex" :class="{ divdisplaynone: currentTab !== 5 }">
          <li
            @click="selectTab(5)"
            class="tabstitle newclass"
            :class="{ newclass2: currentTab == 5 }"
          >
            Completa
          </li>
        </div>
      </ul>
    </div>

    <section v-if="currentTab == 1">
      <div>{{ currentTab }}</div>
    </section>
    <section v-if="currentTab == 2">
      <div>{{ currentTab }}</div>
    </section>
    <section v-if="currentTab == 3">
      <div>{{ currentTab }}</div>
    </section>
    <section v-if="currentTab == 4">
      <div>{{ currentTab }}</div>
    </section>
    <section v-if="currentTab == 5">
      <div>{{ currentTab }}</div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTab: 1
    };
  },
  components: {},

  mounted: function() {},
  methods: {
    selectTab(tabno) {
      this.currentTab = tabno;
    },
    nexttab(tabinfo) {
      //   alert("next called");
      this.currentTab = tabinfo;
    }
  }
};
</script>

<style lang="scss" scoped>
.tabsul {
  list-style: none;
  padding: 0;
  .tabstitle {
    cursor: pointer;
    display: inline-block;
    padding: 1rem;
  }
}
@media screen and (max-width: 600px) {
  .tabsul {
    background: tomato;
    .tabstitle {
      cursor: pointer;
      display: none;
      padding: 1rem;
    }
    .newclass2 {
      display: block;
    }
  }
  .divdisplaynone {
    display: none;
  }
}
</style>
