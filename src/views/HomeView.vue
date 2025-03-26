<template>
  <div id="banner" class="wrapper">
    <section class="banner_heading">
      <div></div>
      <h1>Software Developer<span>Karl John T. Delfin</span></h1>
      <p>I build things for web</p>

      <router-link to="/"
        ><el-button type="primary" round size="large">Hire Me!</el-button></router-link
      >
    </section>

    <section class="banner_image">
      <figure>
        <img src="../assets/images/me.jpg" />
      </figure>
    </section>
  </div>

  <div id="middle">
    <el-carousel height="150px">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3 class="small justify-center" text="2xl">{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
  </div>

  <div id="bottom" class="wrapper">
    <div class="bottom_container">
      <section>
        <h2>Send me a <span>Message</span></h2>
      </section>
      <section>
        <el-form>
          <el-form-item>
            <el-input v-model="email" placeholder="Email" />
          </el-form-item>
          <el-form-item>
            <el-input v-model="message" placeholder="Message" />
          </el-form-item>
          <el-button type="primary" round size="large">Send</el-button>
        </el-form>
      </section>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      email: '',
      message: '',
    }
  },
  mounted() {},
}
</script>

<style>
.wrapper {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* BANNER */
#banner {
  border-bottom: 1px solid white;
  min-height: 600px;
}
.banner_heading {
}
.banner_heading div {
  border-top: 4px solid var(--white);
  width: 150px;
}
.banner_heading h1 {
  font-size: 24px;
  font-weight: 400;
  letter-spacing: 8px;
}
.banner_heading h1 span {
  font-size: 55px;
  display: block;
  font-weight: bold;
  letter-spacing: 0;
}

.banner_heading p {
  margin: 0px;
  font-size: 32px;
  color: #cfd3dc;
}

.banner_heading a {
}
.banner_heading a button {
  width: 150px;
  margin: 20px 0 0;
  font-size: 15px;
}

.banner_image {
}

.banner_image figure {
}

.banner_image figure img {
  height: 100%;
  width: 400px;
  min-width: 100%;
  border-radius: 5px;
}

/* BOTTOM */
#bottom {
  /* min-height: 600px; */
  margin: 30px 0 0;
}
.bottom_container {
  background-color: #fff;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  min-height: 100%;
  border-radius: 5px;
}

.bottom_container section {
  padding: 10px;
  /* margin: 0 0 0 238px; */
}
.bottom_container section h2 {
  font-size: 24px;
  color: var(--blue);
  letter-spacing: 2px;
}
.bottom_container section h2 span {
  display: block;
  font-size: 40px;
  color: var(--black);
  letter-spacing: 0;
}

.bottom_container section form {
  display: flex;
}

.bottom_container section form div {
  margin: 0 5px 0 0;
  width: 360px;
  height: 50px;
}

.bottom_container section form button {
  height: 50px;
  width: 150px;
  font-size: 15px;
}

/* CAROUSEL */
.demonstration {
  color: var(--el-text-color-secondary);
}

.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>
