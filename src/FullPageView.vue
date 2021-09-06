<template>
    <div id="app">
        <ul id="menu">
            <li style="float:left" class="hero">
              <a href="/">
              <img src="./assets/Khervie00_logo.png"  width= "45%" style="margin-top:-25px"/>
              </a>
            </li>
            <div>
            <li data-menuanchor="page1" class="active"><a href="#page1">Overview</a></li>
            <li data-menuanchor="page2"><a href="#page2">Services</a></li>
            <li data-menuanchor="page3"><a href="#page3">Experience</a></li>
            <li data-menuanchor="page4"><a href="#page4">Contact</a></li>
            </div>
        </ul>

    <div class="menu-drawer">
    <a-icon type="menu" @click="showDrawer"/>
    <a-drawer
      title="Basic Drawer"
      :placement="right"
      :closable="false"
      :visible="visible"
      @close="onClose"
    >
        <ul id="side-menu">
            <li data-menuanchor="page1" class="active"><a href="#page1">Overview</a></li>
            <li data-menuanchor="page2"><a href="#page2">Services</a></li>
            <li data-menuanchor="page3"><a href="#page3">Experience</a></li>
            <li data-menuanchor="page4"><a href="#page4">Contact</a></li>
        </ul>
    </a-drawer>
  </div>    

       

        <full-page :options="options" id="fullpage">
            <div class="section">
                 <header-body />
            </div>
            <div class="section">
                <profile />
            </div>
            <div class="section">
                <experience />
            </div>
            <div class="section">
                <contact />
            </div>
        </full-page>
    </div>
</template>

<script>
import HeaderBody from "@/components/HeaderBody.vue"
import Profile from "@/views/Profile.vue"
import Experience from "@/views/Experience.vue"
import Contact from "@/views/Contact.vue"

  export default {
    name: 'app',

    components: {
    HeaderBody,
    Profile,
    Experience,
    Contact,
  },
    data () {
      return {
         visible: false,
        placement: 'left',
        options: {
          licenseKey: 'YOUR_KEY_HERE',
          afterLoad: this.afterLoad,
          scrollOverflow: true,
          scrollBar: false,
          menu: '#menu',
          navigation: true,
          anchors: ['page1', 'page2', 'page3', 'page4'],
        //   sectionsColor: ['#41b883', '#ff5f45', '#0798ec', '#fec401', '#1bcee6', '#ee1a59', '#2c3e4f', '#ba5be9', '#b4b8ab']
        }
      }
    },

    methods: {
    showDrawer() {
      this.visible = true;
    },
    onClose() {
      this.visible = false;
    },
    onChange(e) {
      this.placement = e.target.value;
    },

      afterLoad () {
        console.log('After load')
      },

      addSection (e) {
        e.preventDefault()
        var newSectionNumber = document.querySelectorAll('.fp-section').length + 1

        // creating the section div
        var section = document.createElement('div')
        section.className = 'section'
        section.innerHTML = `<h3>Section ${newSectionNumber}</h3>`

        // adding section
        document.querySelector('#fullpage').appendChild(section)

        // creating the section menu element
        var sectionMenuItem = document.createElement('li')
        sectionMenuItem.setAttribute('data-menuanchor', 'page' + newSectionNumber)
        sectionMenuItem.innerHTML = `<a href="#page${newSectionNumber}">Section${newSectionNumber}</a>`

        // adding it to the sections menu
        var sectionsMenuItems = document.querySelector('#menu')
        sectionsMenuItems.appendChild(sectionMenuItem)

        // adding anchor for the section
        this.options.anchors.push(`page${newSectionNumber}`)

        // we have to call `update` manually as DOM changes won't fire updates
        // requires the use of the attribute ref="fullpage" on the
        // component element, in this case, <full-page>
        // ideally, use an ID element for that element too
        this.$refs.fullpage.build()
      },
      removeSection () {
        var sections = document.querySelector('#fullpage').querySelectorAll('.fp-section')
        var lastSection = sections[sections.length - 1]

        // removing the last section
        lastSection.parentNode.removeChild(lastSection)

        // removing the last anchor
        this.options.anchors.pop()

        // removing the last item on the sections menu
        var sectionsMenuItems = document.querySelectorAll('#menu li')
        var lastItem = sectionsMenuItems[sectionsMenuItems.length - 1]
        lastItem.parentNode.removeChild(lastItem)
      },
      toggleNavigation () {
        this.options.navigation = !this.options.navigation
      },
      toggleScrollbar () {
        console.log('Changing scrollbar...')
        this.options.scrollBar = !this.options.scrollBar
      }
    }
  }
</script>

<style>


    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }

    .menu-drawer{
      display: none;
    }

@media (max-width:576px) {
  .hero{
    margin-left: -50px !important;
  }
}
@media (max-width:768px) {
  .menu-drawer{
    display: block;
  }
  .menu-drawer i{
    float: right;
    margin: 30px;
  }
  .menu-drawer i svg{
    width: 1.4em !important;
    height: 1.4em !important;
  }
  #menu div{
    display: none;
  }
}

</style>
