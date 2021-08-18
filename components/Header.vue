<template>
  <header>
    <div class="header-container">
      <div class="left-header-content">
        <search-icon />
        <input type="search" placeholder="search..." />
      </div>
      <div class="right-header-content">
        <notification-icon />
        <info-icon />
        <user-icon />
      </div>
    </div>
  </header>
</template>

<script>
import SearchIcon from './searchIcon.vue'
import InfoIcon from './infoIcon.vue'
import NotificationIcon from './notificationIcon.vue'
export default {
  components: { SearchIcon, NotificationIcon, InfoIcon },
}
</script>
