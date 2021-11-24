<template>
  <div class="workingWithUs">
    <div class="textContainer">
      <h2 class="my-3"> {{sectionTitle}} <strong class="fst-italic">a message!</strong></h2>
      <p class="py-3 m-0">{{sectionInfo}}</p>
      <button class="btn mt-3">CONTACT</button>
    </div>
  </div>
</template>

<script>

export default {
  name: 'WorkingWithUs',
  data(){
    return{
      sectionTitle: 'Want to work with us? send us ',
      sectionInfo:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste voluptatibus, qui unde voluptates laudantium, maxime quam consequatur quibusdam veritatis beatae quaerat fugit ad accusamus est delectus nam natus officia atque?',
    };
  },
}
</script>

<style lang='scss'>
.workingWithUs{
  background: url('../assets/img/work_with_us-bg.png');
  background-size: cover;
  padding: 100px 0;

  .textContainer{
    max-width: 75%;
    margin: auto;
    
    h2{
      font-size: 60px;
      font-weight: normal;
    }
    p{
      font-size: 20px;
      color: #878787;
    }
    button{
      background-color: rgb(216, 240, 227);
      padding: 15px 50px;
      position: relative;

      &:focus{
        box-shadow: none;
      }

      &:hover{
        // background: rgb(239, 205, 190);
        background: radial-gradient(circle closest-corner at 147px 41px, #F5D8CA 25%, #E1C0B0 35%);
      }

    }
  }
}
</style>