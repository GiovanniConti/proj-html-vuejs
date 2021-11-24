<template>
  <footer>
    <div class="container-xl d-flex justify-content-between py-5">

      <ul>
        <li><img src="@/assets/img/logo-sidearea-1.png" alt="logo-footer"></li>
        <li>Let's Get Creative</li>
      </ul>

      <ul
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

      <ul>
        <li>Stay in touch with us</li>
        <li class="">
          <i class="fa fa-twitter" aria-hidden="true"></i>
          <i class="fa fa-pinterest-p" aria-hidden="true"></i>
          <i class="fa fa-facebook" aria-hidden="true"></i>
          <i class="fa fa-linkedin" aria-hidden="true"></i>
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
      footerList: [
        'maree.qode@gmail.com',
        '+44645 321 789',
        "Avenue d'Auderghem 10",
        '1040 Brussels, Belgium',
        'Stay in touch with us',
      ],
      contactsInfo: ["maree.qode@gmail.com", "+44645 321 789"],
      addressInfo: ["Avenue d'Auderghem 10", "1040 Brussels, Belgium"],

      footerInfo: [
        {
          info1: "maree.qode@gmail.com",
          info2: "+44645 321 789",
        },
        {
          info1: "Avenue d'Auderghem 10",
          info2: "1040 Brussels, Belgium",
        },
      ]
    };
  },
  methods: {

  }
}
</script>

<style lang="scss">
footer{
  background-color: rgb(192, 225, 207);

  .container-xl{

    ul{
      list-style: none;

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