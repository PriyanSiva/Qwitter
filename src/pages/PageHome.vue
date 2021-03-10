<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input 
        bottom-slots 
        v-model="newQweetContent" 
        placeholder="What's happening?" 
        counter maxlength="280"
        autogrow
        class="new-qweet"
        >
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg">
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink q-mb-lg">
          <q-btn unelevated rounded color="primary" label="Qweet" no-caps />
      </div>

    </div>

    <q-separator size="10px" color="grey-2" class="divider" />

    <q-list>

      <q-item class="q-py-md">
        <q-item-section avatar top>
         <q-avatar size="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg">
            </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong>User Name</strong>
            <span class="text-grey-7 q-ml-sm">@username</span> 
          </q-item-label>
          <q-item-label class="qweet-content text-body1">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere, eligendi dolore. 
            
            Tempora odit facilis voluptate quidem, libero autem evenietea similique excepturi quo aliquid consequatur,nam temporibus recusandae voluptates impedit!
          </q-item-label>
        </q-item-section>

        <q-item-section side top>
          1 min ago
        </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
export default {
  name: 'PageHome',
  data() {
    return{
      newQweetContent: ''
    }
  }
}
</script>

<style lang="sass" scoped>
.new-qweet
    font-size: 19px
  
.divider
  border-bottom: 1px solid
  border-top: 1px solid
  border-color: $grey-4

.qweet-content
  white-space: pre-line
</style>
