<script>
import Tab from '../components/Tab.vue'
import Tabs from '../components/Tabs.vue'
import Test from '../views/Test.vue'

export default {
  components: {
    Tab,
    Tabs,
    Test,
  },
  data() {
    return {
      activeTab: 'tab1'
    }
  },
  methods: {
    changeStyle() {
      if (this.mode === 'dark') {
        this.mode = 'light'
      } else {
        this.mode = 'dark'
      }
    }
  }
}
</script>

<template>
  <div class="container">
    <ul class="nav nav-tabs">
      <li class="nav-item">
        <a class="nav-link" :class="{ active: activeTab === 'tab1' }" 
        @click="activeTab = 'tab1'" aria-current="page" href="#">MnM</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" :class="{ active: activeTab === 'tab2' }" 
        @click="activeTab = 'tab2'" href="#">Kompos(dot)com</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" :class="{ active: activeTab === 'tab3' }" 
        @click="activeTab = 'tab3'" href="#">Trading</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" :class="{ active: activeTab === 'tab4' }" 
        @click="activeTab = 'tab4'" href="#">Exflora</a>
      </li>
    </ul>

    <div class="tab-content">
      <div v-if="activeTab === 'tab1'" class="tab-pane active"><Test/></div>
      <div v-if="activeTab === 'tab2'" class="tab-pane active">Content for Tab 2</div>
      <div v-if="activeTab === 'tab3'" class="tab-pane active">Content for Tab 3</div>
      <div v-if="activeTab === 'tab4'" class="tab-pane active">Content for Tab 4</div>
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: 'Karla', sans-serif;
}

.wrapper {
  width: 100%;
  min-height: 100vh;
  background-color: #f8f8f8;
  margin: 0;
  padding: 20px;
}

.change__style {
  background-color: #eee;
  font-size: 1em;
  margin-bottom: 10px;
  padding: 5px;
}
</style>