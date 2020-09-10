<template>
  <div id="app" class="flex container h-screen w-full">
    <!-- side nav -->
    <div class="lg:w-1/5 border-r border-lighter px-2 lg:px-6 py-2 flex flex-col">
      <button class="h-12 w-12 hover:bg-lightblue text-3xl text-blue rounded-full">
        <font-awesome-icon :icon="['fab', 'twitter']" />
      </button>
      <div>
        <button v-for="tab in tabs" :key="tab.icon" class="hover:text-blue flex items-center py-2 px-4 hover:bg-lightblue rounded-full mr-auto mb-3">
          <i :class="`${ tab.icon } text-2xl mr-4`"></i>
          <p class="text-lg font-semibold text-left"> {{ tab.title }} </p>
        </button>
      </div>
    </div>
    
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      tabs: [
        {icon: 'fas fa-home', title: 'Home', id:'home'},
        {icon: 'fas fa-hashtag', title: 'Explore', id: 'explore'},
        {icon: 'far fa-bell', title: 'Notifications', id: 'notifications'},
        {icon: 'far fa-envelope', title: 'Messages', id: 'messages'},
        {icon: 'far fa-bookmark', title: 'Bookmarks', id: 'bookmarks'},
        {icon: 'fas fa-clipboard-list', title: 'Lists', id: 'lists'},
        {icon: 'far fa-user', title: 'Profile', id: 'profile'},
        {icon: 'fas fa-ellipsis-h', title: 'More', id: 'more'}
      ]
    }
  },

}

</script>

