<template>
	<div>
		<div>
      <b-navbar toggleable="lg" type="dark" variant="dark">
        <b-navbar-brand ><span style="cursor:pointer;" @click="managesidebar">&#9776;</span>
        </b-navbar-brand>

        <b-navbar-toggle target="nav_collapse" />

        <b-collapse is-nav id="nav_collapse">
          <b-navbar-nav>
            <b-nav-item href="#">
            	<img src="@/assets/logo.jpg" style="height:30px; width:285px">
            </b-nav-item>
            <b-nav-item href="#" disabled>Disabled</b-nav-item>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-form>

               <b-form-input id="large"  class=" mr-sm-2 " type="text" placeholder="Search" />

              <!-- <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button> -->
            </b-nav-form>

            <!-- <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown> -->

            <b-nav-item-dropdown right>
              <!-- Using button-content slot -->
              <template slot="button-content"><em>User</em></template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item @click="signout">Signout</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
	</div>
</template>
<script type="text/javascript">
	export default{
		props:['shown','logseen'],
		methods:{
			managesidebar(){
				this.shown = !this.shown
				this.$emit('flagwasupdated', this.shown)
			},
			signout(){
				this.logseen =! this.logseen;
				this.$emit('logseenupdated', this.logseen)
			}
		}
	}
</script>
<style>
	#large{
		width: 500px;
	}
</style>
