<template>
  <div class="blogHighlights">
    <div class="container-xl">
      <div class="row row-cols-3">
        <div class="col"
          v-for="(article, i) in highlightsList"
          :key="i"
        >
          <div class="card px-1">
            <img class="card-img-top"  :src="require('@/assets/img/' + article.img)" :alt="article.img">
            <div class="card-body text-start p-0 pt-4">
              <h5 class="card-title mb-3 fw-bold">{{ article.details }}</h5>
              <h6 class="card-text fw-normal fst-italic">By {{ article.signature }}</h6>
            </div>
          </div>

          <div class="ribbonContainer">
            <h2 class="ribbon-day">07</h2>
            <div class="ribbon">
              <h6 class="ribbon-month">MAY'19</h6>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlogHighlights',
  data(){
    return{
      highlightsList: [
        {
          img: 'h-2-blog-img-1.jpg',
          details: 'This way, loves: a detailed guide through new design',
          signature: 'Emily Fields',
        },
        {
          img: 'h-2-blog-img-2.jpg',
          details: 'I try to give people a different way of looking art',
          signature: 'Emily Fields',
        },
        {
          img: 'h-2-blog-img-3.jpg',
          details: 'Introduce Richard Laperrière of those amazing features',
          signature: 'Emily Fields',
        },
      ]
    };
  },
}
</script>

<style lang='scss'>
.blogHighlights{
  padding: 130px 0;

  .container-xl{
    .row{
      .col{
        position: relative;

        .card{
          border: 0;
          border-radius: 0;

          .card-img-top{
            border-radius: 0;
          }
        }

        .ribbonContainer{
          width: 60px;
          height: 80px;
          position: absolute;
          top: -15px;
          left: 30px;

          .ribbon-day{
            padding: 5px 0;
            font-style: italic;
            background-color: rgb(192, 225, 207);
            margin-bottom: 0;
            font-size: 25px;
          }

          .ribbon{
            width: 60px;
            height: 40px;
            border: (60px * .5) solid rgb(243, 208, 199);
            border-bottom: 10px solid transparent;
            border-top: none;

            .ribbon-month{
              font-size: 12px;
              font-weight: bold;
              margin-left: 60px * -.5;
              padding-top: 5px;
              padding-left: 8px;
            }
          }
        }
      }
    }
  }
}

</style>