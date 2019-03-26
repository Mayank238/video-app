<template>
  <div >
    <sidebar-menu :menu="menu" class="space" />
  </div>
</template>

<script>
    export default {
        data() {
            return {
                menu: [
                    {
                        header: true,
                        title: 'Main Navigation',
                        // component: componentName
                        // visibleOnCollapse: true
                    },
                    {
                        href: '/',
                        title: 'Home',
                        icon: 'fa fa-home',
                        /*
                        disabled: true
                        badge: {
                            text: 'new',
                            // class:''
                        }
                        */
                    },
                    {
                        title: 'Trending',
                        icon: 'fa fa-trend',
                        child: [
                            {
                                href: '/charts/sublink',
                                title: 'Sub Link',
                            }
                        ]
                    },
                    {
                        title: 'Courses',
                        icon: 'fa fa-trend',
                    }
                ]
            }
        }
    }
</script>
<style>
.space{
    position:relative;
}
</style>
