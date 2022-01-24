<template>
  <div class="home">
    <section class="overview">
      <span class="span">SO, YOU WANT TO TRAVEL TO</span>
      <h1 class="title">SPACE</h1>
      <p class="paragraph">
        Let’s face it; if you want to go to space, you might as well genuinely
        go to outer space and not hover kind of on the edge of it. Well sit
        back, and relax because we’ll give you a truly out of this world
        experience!
      </p>
    </section>
    <button class="btn btn-main">EXPLORE</button>
  </div>
</template>

<script>
export default {
  name: 'AppHome',
}
</script>

<style>
.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url('@/assets/home/background-home-mobile.jpg');
  justify-content: space-between;
  background-repeat: no-repeat;
  height: 667px;
  width: 100%;
}

.title {
  font-size: 80px;
  line-height: 100px;
  margin: 16px 0;
}

.overview {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 112px 22px 0;
}

.span {
  font-family: 'Barlow Condensed', sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 19px;
  text-align: center;
  letter-spacing: 2.7px;
  color: var(--light-blue);
  margin: 0;
}

.paragraph {
  text-align: center;
  font-size: 15px;
  line-height: 25px;
  margin: 0;
}

.btn {
  border-radius: 50%;
  border-style: none;
  font-family: Bellefair, serif;
  font-style: normal;
  font-weight: normal;
  color: var(--black);
  background-color: var(--white);
  cursor: pointer;
}

.btn-main {
  margin: 0;
  margin-bottom: 48px;
  width: 150px;
  height: 150px;
  font-size: 20px;
  transition: box-shadow 0.6s;
}

.btn-main:hover {
  box-shadow: 0 0 0 40px #aaa;
}

@media (min-width: 376px) {
  .home {
    background-image: url('@/assets/home/background-home-tablet.jpg');
    height: 1024px;
  }

  .overview {
    margin: 202px 24px 0;
    width: 450px;
  }

  .title {
    font-size: 150px;
    line-height: 150px;
  }

  .span {
    font-size: 20px;
    line-height: 24px;
  }

  .paragraph {
    font-size: 16px;
    line-height: 28px;
  }

  .btn-main {
    margin: 0;
    margin-bottom: 90px;
    width: 246px;
    height: 246px;
    font-size: 32px;
    line-height: 37px;
  }
}

@media (min-width: 769px) {
  .home {
    background-image: url('@/assets/home/background-home-desktop.jpg');
    height: 900px;
    max-width: 1440px;
    align-items: flex-end;
    flex-flow: wrap row;
    justify-content: space-between;
  }

  .overview {
    margin: 0;
    width: 450px;
    margin-left: 9%;
    margin-bottom: 9%;
    align-items: flex-start;
  }

  .title {
    font-size: 150px;
    line-height: 172px;
  }

  .span {
    font-size: 28px;
    line-height: 34px;
    text-align: left;
  }

  .paragraph {
    font-size: 17px;
    line-height: 32px;
    text-align: left;
  }

  .btn-main {
    margin: 0 9% 9%;
    width: 246px;
    height: 246px;
    font-size: 32px;
    line-height: 37px;
  }
}
</style>
