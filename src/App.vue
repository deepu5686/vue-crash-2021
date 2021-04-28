<template>
  <div class="container">
    <Header 
    @toggle-add-task="toggleAddTask" 
     :showAddTask="showAddTask"
    title="Task Traker"/>
    <router-view :showAddTask="showAddTask"></router-view>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header';
import Footer from './components/Footer';
export default {
  name: 'App',
  components: {
    Header,
    Footer
  },
  data() {
      return {
        showAddTask: false
      }
  },
  methods: {
     toggleAddTask(){
        
      this.showAddTask =  !this.showAddTask
    },
  }
}
</script>

