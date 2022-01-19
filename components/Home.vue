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
  background-repeat: no-repeat;

  /* background-size: contain; */
  height: 667px;
  width: 100%;
}

.title {
  font-size: 80px;
  line-height: 100px;
  margin: 16px 24px;
}

.overview {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 112px 24px;
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
}

.paragraph {
  text-align: center;
  font-size: 15px;
  line-height: 25px;
  margin: 0 24px;
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
  margin-top: 50px;
  width: 150px;
  height: 150px;
  font-size: 20px;
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
    margin: 202px 159px;
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
    margin-top: 156px;
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
    flex-direction: row;
    align-items: flex-end;
    justify-content: space-between;
  }

  .overview {
    margin: 0;
    width: 450px;
    margin-left: 131px;
    margin-bottom: 165px;
  }

  .title {
    font-size: 150px;
    line-height: 172px;
  }

  .span {
    font-size: 28px;
    line-height: 34px;
  }

  .paragraph {
    font-size: 18px;
    line-height: 32px;
  }

  .btn-main {
    margin: 0;
    margin-right: 131px;
    margin-bottom: 165px;
    width: 246px;
    height: 246px;
    font-size: 32px;
    line-height: 37px;
  }
}
</style>
