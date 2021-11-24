<template>
  <footer>
    <div class="container-xl d-flex justify-content-between py-5">
      <!-- Logo list -->
      <ul>
        <li><img src="@/assets/img/logo-sidearea-1.png" alt="logo-footer"></li>
        <li>Let's Get Creative</li>
      </ul>
      <!-- Info array lists -->
      <ul class="text-start"
        v-for="(item, i) in footerInfo"
        :key="i"
      >
        <li
          v-for="(info, j) in item"
          :key="j"
        >
          {{info}}
        </li>
      </ul>
      <!-- social list -->
      <ul>
        <li>Stay in touch with us</li>
        <li>
          <i
            v-for="(icon, i) in socialsIconsList"
            :key="i"
            :class="icon" aria-hidden="true"></i>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {

  },
  data() {
    return {
      footerInfo: [
        {
          info1: "maree.qode@gmail.com",
          info2: "+44645 321 789",
        },
        {
          info1: "Avenue d'Auderghem 10",
          info2: "1040 Brussels, Belgium",
        },
      ],
      socialsIconsList: [
        "fa fa-twitter",
        "fa fa-pinterest-p",
        "fa fa-facebook",
        "fa fa-linkedin",
      ],
    };
  },
  methods: {

  }
}
</script>

<style lang="scss">
footer{
  background-color: #C0E1CF;

  .container-xl{

    ul{
      list-style: none;
      margin: 0;
      padding-top: 15px;

      li{
        padding-bottom: 15px;

        i{
          margin: 0 15px;
          cursor: pointer;
        }
      }
    }
  }
}
</style>