<template>
  <div>
    <h3>Write your Review</h3>
    <p>
      Your email address will not be published. Required fields are marked with
      *
    </p>
    <h3>Your Ratings</h3>
    <form class="opinion-form">
      <div class="o-rating">
        <ul class="opinion-rating stars-rating">
          <li>
            <a href="#">
              <i class="icon-star" />
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-star" />
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-star" />
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-star" />
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-star" />
            </a>
          </li>
        </ul>
      </div>
      <b-form-textarea
        id="textarea"
        type="text"
        placeholder="Your review...*"
      />
      <div class="disp-flex-2">
        <b-form-input type="text" placeholder="Name*" />
        <b-form-input type="email" placeholder="Email*" />
      </div>
      <b-form-file placeholder="Upload Your image or drop it here...*" />
      <button type="submit" class="a-dark">
        Submit
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'WriteOpinion'
}
</script>

<style lang="less" scoped>
.disp-flex-2 {
  display: flex;
  justify-content: space-between;
  input {
    width: 48%;
  }
}
textarea {
  height: 130px;
}
.opinion-form {
  margin-top: 10px;
}
h3 {
  margin-bottom: 20px;
}
.a-dark {
  margin-top: 30px;
  display: block;
}
/deep/ .opinion-rating {
  justify-content: flex-start;
}
</style>
