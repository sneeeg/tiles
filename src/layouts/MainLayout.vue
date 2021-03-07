<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-toolbar-title>
          <div class="text-subtitle2 header_subtitle">Персонал</div>
          <div class="text-h6 header_title">Персонал</div>
        </q-toolbar-title>
        <div class="header-search">
          <input class="q-mr-md" type="text" placeholder="Поиск/фильтр">
          <q-btn style="color: #8091A5" flat round color="black" icon="tune" @click="leftDrawerOpen = !leftDrawerOpen" />
        </div>
      </q-toolbar>
    </q-header>

    <q-footer >
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          style="color:#8091A5"
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <div class="text-body2 q-ml-sm" style="color:#8091A5">Всего сотрудников</div>
      </q-toolbar>
    </q-footer>

    <q-drawer
      side="right"
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Информация
        </q-item-label>
        <q-separator />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

const linksData = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  }
]

export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>

<style lang="sass" scoped>
header
  display: flex
  justify-content: space-between
  align-items: center
  background-color: #fff
  height: 55px
  margin-top: 30px

footer
  height: 40px
  background: #E9EEF3
  display: flex
  align-items: center

.header_title
  font-weight: 500
  color: #3F4A56
  font-size: 25px

.header_subtitle
  color: #8091A5
  font-weight: 500
  font-size: 12px

.header-search
  height: 100%
  padding: 5px 35px
  border-left: 1px solid #E9EEF3
</style>
