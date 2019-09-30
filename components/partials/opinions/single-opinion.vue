<template>
  <div class="single-opinion">
    <h3>3 reviews for White Striped top</h3>

    <div class="opinion-block">
      <div class="left">
        <div class="left-image">
          <b-img src="~assets/img/listing/product-1.jpg" alt="image" />
        </div>
      </div>
      <div class="right">
        <div class="o-rating">
          <ul class="opinion-rating stars-rating">
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
          </ul>
        </div>
        <h5>John Connor- <span>Dec 25th,2018</span></h5>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae ipsum
          perspiciatis, impedit laboriosam commodi in excepturi porro aut
          tempore facilis.
        </p>
      </div>
    </div>

    <div class="opinion-block">
      <div class="left">
        <div class="left-image">
          <b-img src="~assets/img/listing/product-5.jpg" alt="image" />
        </div>
      </div>
      <div class="right">
        <div class="o-rating">
          <ul class="opinion-rating stars-rating">
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
            <li><i class="icon-star" /></li>
          </ul>
        </div>
        <h5>Joanna Connor- <span>Dec 25th,2018</span></h5>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae ipsum
          perspiciatis, impedit laboriosam commodi in excepturi porro aut
          tempore facilis.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SingleOpinion'
}
</script>

<style lang="less" scoped>
.single-opinion {
  margin-bottom: 80px;
}
.opinion-block {
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  margin-bottom: 30px;
}
.left-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  overflow: hidden;
  margin-right: 100px;
  img {
    display: block;
    max-width: 100%;
    height: auto;
    border-radius: 50%;
  }
}
.o-rating {
  margin-bottom: 5px;
}
.stars-rating {
  justify-content: flex-start;
}
h5 {
  margin-bottom: 10px;
  span {
    color: @color-primary-i;
    font-size: 15px;
  }
}
</style>
