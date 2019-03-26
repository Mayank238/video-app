<template>
  <div>
    <div v-if="firstseen">
      <app-login></app-login>
    </div>
    <div v-if="!firstseen">
      <div>
        <app-header :shown="flag" @flagwasupdated="flagupdate"></app-header>
      </div>
      <div v-if="flag">
        <app-sidebar class="space"></app-sidebar>
      </div>
    </div>
  </div>
</template>
<script type="text/javascript">
import header from '@/components/Header'
import sidebar from '@/components/sidebar'
import login from '@/components/login'
  export default{
    data(){
      return{
          flag:true,
          firstseen:true
      }
    },
    components:{
      'app-header': header,
      'app-sidebar': sidebar,
      'app-login': login
    },
    methods:{
      flagupdate(value){
        this.flag=value;
      }
    }
  }
</script>
