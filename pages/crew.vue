<template>
  <div class="crew">
    <section class="header">
      <span class="header-title header-title-opacity">02</span>
      <h1 class="header-title">MEET YOUR CREW</h1>
    </section>
    <section class="image-container">
      <img :src="crewPicture" alt="crew member picture" class="image" />
    </section>
    <section class="indicators">
      <span class="indicator"></span>
      <span class="indicator"></span>
      <span class="indicator"></span>
      <span class="indicator"></span>
    </section>
    <section class="member-description">
      <h2 class="crew-grade">{{ crewGrade }}</h2>
      <h2 class="crew-member">{{ crewMember }}</h2>
      <p class="crew-summary">{{ crewSummary }}</p>
    </section>
  </div>
</template>

<script>
import douglasImg from '@/assets/crew/image-douglas-hurley.png'
export default {
  name: 'CrewPage',
  data: () => {
    return {
      crewMember: 'DOUGLAS HARLEY',
      crewPicture: douglasImg,
      crewGrade: 'COMMANDER',
      crewSummary:
        'Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He launched into space for the third time as commander of Crew Dragon Demo-2.',
    }
  },
}
</script>

<style>
.crew {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url('@/assets/crew/background-crew-mobile.jpg');
  justify-content: flex-start;
  gap: 32px;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  height: 100vh;
  width: 100%;
}

.header {
  display: flex;
  flex-direction: row;
  margin-top: 88px;
}

.header-title {
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

.header-title-opacity {
  opacity: 0.25;
  margin-right: 16px;
}

.image-container {
  display: flex;
  justify-content: center;
  width: 90vw;
  border-bottom: #383b4b solid 1px;
}

.image {
  max-height: 223px;
}

.indicators {
  display: flex;
  flex-flow: row;
  justify-content: space-around;
  width: 88px;
}

.indicator {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  border-style: none;
  background-color: var(--white);
  cursor: pointer;
  opacity: 0.17;
}

.crew-grade {
  font-size: 16px;
  line-height: 18px;
  text-align: center;
  opacity: 0.5;
  margin-bottom: 8px;
}

.crew-member {
  font-size: 24px;
  line-height: 28px;
  text-align: center;
}

.crew-summary {
  font-size: 15px;
  line-height: 25px;
  text-align: center;
  max-width: 327px;
  margin-top: 16px;
}

@media (min-width: 600px) {
  .crew {
    background-image: url('@/assets/crew/background-crew-tablet.jpg');
  }

  .header-title {
    font-size: 20px;
    line-height: 24px;
  }

  .image-container {
    margin-top: 8px;
    order: 3;
    overflow: hidden;
  }

  .image {
    max-height: 572px;
    object-fit: cover;
  }

  .indicators {
    order: 2;
  }

  .header {
    align-self: flex-start;
    margin-top: 136px;
    margin-left: 38.5px;
  }

  .crew-grade {
    font-size: 24px;
    line-height: 28px;
  }

  .crew-member {
    font-size: 40px;
    line-height: 46px;
  }

  .crew-summary {
    font-size: 16px;
    line-height: 28px;
    max-width: 458px;
  }
}

@media (min-width: 980px) {
  .crew {
    max-width: 1920px;
    background-image: url('@/assets/crew/background-crew-desktop.jpg');
    align-items: flex-start;
    flex-flow: wrap column;
    justify-content: flex-end;
  }

  .header {
    margin-left: 166px;
    margin-bottom: 9vh;
    margin-top: 7%;
  }

  .header-title {
    font-size: 28px;
    line-height: 34px;
  }

  .image-container {
    margin-right: 9vw;
    width: fit-content;
  }

  .indicators {
    margin-top: 7vh;
    margin-bottom: 5vh;
    margin-left: 167px;
  }

  .member-description {
    margin-left: 165px;
  }

  .crew-grade {
    font-size: 32px;
    line-height: 37px;
    text-align: left;
    margin-bottom: 15px;
  }

  .crew-member {
    font-size: 56px;
    line-height: 64px;
    text-align: left;
    margin-bottom: 27px;
  }

  .crew-summary {
    font-size: 18px;
    line-height: 32px;
    text-align: left;
    max-width: 458px;
  }
}
</style>