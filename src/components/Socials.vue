<template>
  <div>
    <ul id="example-2" style="display: grid;grid-template-columns:repeat(30,1fr);">
        <li class="d-inline-flex" v-for="(item) in mediaHandles"  v-bind:key="item">
            <a :href="item.url">
              <b-icon :icon="item.icon"></b-icon>
            </a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
          mediaHandles: [
        {
            name: "Twitter",
            url: "https://twitter.com/Kwesi_Hervie?s=08",
            icon:"twitter",
        },
           {
            name: "LinkedIn",
            url: "https://www.linkedin.com/in/kwesi-hervie-10622715b/",
            icon:"linkedin",
        },
           {
            name: "Github",
            url: "https://github.com/khervie-star",
            icon:"github",
        },
           {
            name: "Facebook",
            url: "https://www.facebook.com/bradley.mathman",
            icon:"facebook",
        },
           {
            name: "Instagram",
            url: "https://www.instagram.com/hey_smiths/",
            icon:"instagram",
        },
    ]
    }
  }
}
</script>

<style scoped>
ul{

}
li{
  border: 2px solid;
  border-color: inherit;
  width: 40px;
  height: 40px;
  align-items: center;
  justify-content: center;
  justify-items: center;
  border-radius: 50%;
  margin: 0 5px;
}

a{
  color: inherit;
}
</style>