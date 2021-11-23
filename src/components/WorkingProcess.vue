<template>
  <div class="sectionWorkingPocess py-5 my-4">
    <h2 class="sectionTitle m-0">Working <strong class="fst-italic">process</strong></h2>

    <div class="container-xl py-5">
      <div class="row">
        <div class="col-3 wp_card d-flex flex-column align-items-center"
          v-for="(item, i) in workingProcessList"
          :key="i"
        >
        <div class="iconContainer text-center">
          <a href="#"><i class="fa fa-lightbulb-o" aria-hidden="true"></i></a>
        </div>
          <h3 class="fs-5 my-2">{{item.title}}</h3>
          <p class="">{{item.detail}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WorkingProcess',
  props: {

  },
  data() {
    return {
      workingProcessList: [
        {
          icon: '<i class="fa fa-lightbulb-o" aria-hidden="true"></i>',
          title: 'First theres an idea',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: '<i class="fa fa-comment-o" aria-hidden="true"></i>',
          title: 'Then we talk about',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: '<i class="fa fa-cloud" aria-hidden="true"></i>',
          title: 'And we think about',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: '<i class="fa fa-pencil" aria-hidden="true"></i>',
          title: 'So we draw along',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
      ],
    };
  },
}
</script>

<style lang="scss">
.sectionWorkingPocess{

  .sectionTitle{
    font-size: 60px;
  }

  .container-xl{
    background: url('../assets/svg/svg-3.svg');
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: 35px;
    
    .row{
      .wp_card{
        .iconContainer{
          width: 120px;
          height: 120px;
          border-radius: 50%;
          background-color: rgb(250, 247, 241);

          a{
            i{
              line-height: 120px;
              vertical-align: middle;
              font-size: 50px;
              color: rgb(192, 225, 207);
            }
          }
        }

        p{
            font-size: 14px;
            color: rgb(150, 150, 150);
          }
      }
    }
  }
}

</style>