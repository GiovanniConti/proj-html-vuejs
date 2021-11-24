<template>
  <div class="sectionWorkingPocess py-5 my-4">
    <h2 class="sectionTitle m-0 fw-normal">Working <strong class="fst-italic">process</strong></h2>

    <div class="container-xl py-5">
      <div class="row">
        <div class="col-3 wp_card d-flex flex-column align-items-center"
          v-for="(item, i) in workingProcessList"
          :key="i"
        >
        <div class="iconContainer text-center">
          <a href="#"><i class="cardIcon" :class="item.icon" aria-hidden="true"></i></a>
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
          icon: 'fa fa-lightbulb-o',
          title: 'First theres an idea',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: 'fa fa-comment-o',
          title: 'Then we talk about',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: 'fa fa-cloud',
          title: 'And we think about',
          detail: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, dolorem?',
        },
        {
          icon: 'fa fa-pencil',
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
          background-color: #FAF7F1;

          a{
            .cardIcon{
              line-height: 120px;
              vertical-align: middle;
              font-size: 50px;
            }
          }
        }

        p{
            font-size: 14px;
            color: #878787;
          }
      }
      .wp_card:nth-child(1) .cardIcon{
        color: #C0E1CF;
      }
      .wp_card:nth-child(2) .cardIcon{
        color: #F8D12D;
      }
      .wp_card:nth-child(3) .cardIcon{
        color: #80465F;
      }
      .wp_card:nth-child(4) .cardIcon{
        color: #EB6950;
      }
    }
  }
}

</style>