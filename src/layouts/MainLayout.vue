<template>
  <q-layout view="lHr lpR fFf">

    <q-header bordered class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title class="text-weight-bold">
          <span class="gt-sm">
            {{ $route.name }}
          </span> 
           <q-icon 
            class="q-pa-md header-icon lt-md"
            name="fas fa-dove"
            size="sm"
            color="primary"
          />
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer 
      show-if-above 
      v-model="left" 
      side="left" 
      bordered
      :width="283"
    >
      <q-icon 
        class="q-pa-md"
        name="fas fa-dove"
        size="md"
        color="primary"
      />

      <q-list>
        
        <q-item 
          to="/"
          clickable 
          v-ripple
          exact
        >
          <q-item-section avatar>
            <q-icon name="home" size="md"/>
          </q-item-section>

          <q-item-section class="text-h6 font-weight-bold">Home</q-item-section>
        </q-item>

        <q-item 
          to="/about"
          clickable 
          v-ripple
          exact
        >
          <q-item-section avatar>
            <q-icon name="help" size=md />
          </q-item-section>

          <q-item-section class="text-h6 font-weight-bold">About</q-item-section>
        </q-item>

      </q-list>


    </q-drawer>

    <q-drawer show-if-above v-model="right" side="right" bordered>

      <q-input 
        color="teal" 
        placeholder="search" 
        dense 
        class="q-ma-md" 
        outlined 
        rounded>
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>

      <q-list padding separator>
        <q-item>
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="font-weight-bold">Single line item</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>

        <q-item>
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="font-weight-bold">Single line item</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>

        <q-item>
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="font-weight-bold">Single line item</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>

    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      left: false,
      right: false
    }
  }
}
</script>

<style lang="sass" scoped>

.header-icon 
  position: absolute
  bottom: 0
  left: 50%
  transform: translateX(-50%)
</style>