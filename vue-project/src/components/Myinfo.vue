<script setup>
import { infoSkill } from '@/constants/index'
</script>

<template>
  <section id="My_info">
    <div class="My_info__inner">
      <h2 class="My_info__title">introduce <em>나는 누구인가</em></h2>
    </div>
    <div class="about_ctn_sub">
      <div class="about-my">
        <div class="img-txt">
          <figure>
            <img src="../assets/img/profile2.png" alt="" />
          </figure>
          <div class="text">
            <p>
              처음은 누구나 <br />
              어렵고 힘들지만 <br />
              고수들도 삽질은 언제나 한다<br />
              열심히 공부하자
            </p>
          </div>
        </div>
        <div class="history">
          <div class="nameYE">
            <h4>황의철</h4>
            <div class="yearEmail">
              <p>생년월일 : (남) 1993년생</p>
              <p>|</p>

              <a href="mailto:icucheol@gmail.com">
                <p class="email">E-mail : icucheol@gmail.com</p></a
              >
            </div>
          </div>
          <dl>
            <dt>학력사항</dt>
            <dd>국가평생교육진흥원 산업공학 학사 재학중 2022.03</dd>
            <dt>자격증</dt>
            <dd>물류관리사 2021.07</dd>
            <dd>유통관리사 2급 2021.11</dd>
            <dd>컴퓨터활용능력 1급 2022.06</dd>
            <dd>ITQ OA MASTER 2022.10</dd>
            <dd>SQLD SQL개발자 2022.12</dd>
            <dt>경력사항</dt>
            <dd>중랑식자재 - 유통영업 2016.12 - 2021.12</dd>
            <dd>구일지엘에스 - 물류영업 2023.01 - 2023.05</dd>
          </dl>
        </div>
      </div>
      <div class="about_slide_in_skill">
        <h5>My <b>skills</b></h5>
        <ul class="skill-list">
          <li v-for="(skill, index) in infoSkill" :key="index">
            <figure class="skill-figure">
              <img class="skill-img" :src="skill.src" alt="" />
            </figure>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@import '@/assets/scss/reset';
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif+Display:ital,wght@1,700&display=swap');

.My_info__inner {
  padding: 16px;

  .My_info__title {
    position: sticky;
    top: 70px;
    left: 0;
    width: 70%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    font-family: var(--mainKor-font);
    text-transform: uppercase;
    color: var(--mainKor-font);
    // border-bottom: 0.4vw solid var(--black100);
    border-bottom: 0.4vw solid var(--black100);
    margin-bottom: 100px;

    @media (max-width: 800px) {
      width: 100%;
      margin-bottom: 10vw;
      font-size: 30px;
      height: auto;
      top: 68px;
      z-index: 1000;
      background-color: var(--mainBg-color);
    }

    em {
      font-size: 1.25rem;
      font-weight: 400;
      line-height: 2;
    }
  }

  /* The rest of your styles here */
}

.about_ctn_sub {
  /* width: 100vw; */
  width: 6600px;
  height: 660px;
  display: flex;
  margin-top: -60px;
  padding-left: 100px;
  //   visibility: hidden;
  /* border: 1px solid #000; */
  background: var(--mainBg-color);

  .img-txt {
    width: 200px;
  }

  figure {
    margin-top: 108px;
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    vertical-align: top;
    border: 1px solid var(--mainBg-color);
    border-radius: 85px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: var(--mainBg-color);
  }

  .text {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
  }

  .about-my {
    display: flex;
    // width: 100vw;
    color: #000;
    flex-direction: row;
    flex-wrap: nowrap;
    margin-left: 10px;
    gap: 80px;
  }

  .nameYE {
    display: flex;
    align-items: start;
    gap: 30px;
  }

  h4 {
    font-weight: 500;
    font-size: 24px;
    padding-left: 5px;
  }
  .yearEmail {
    margin-top: 5px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .email {
    cursor: pointer;
  }

  dl {
    margin-top: 15px;
    display: inline-block;
  }

  dt {
    text-align: center;
    width: 95px;
    font-size: 18px;
    font-weight: 600;
    padding: 5px 10px;
    border-radius: 40px;
    border: 2px solid #000;
    margin: 22px 0px 6px 0px;
  }

  dd {
    padding-left: 5px;
    font-size: 16px;
    margin-top: 4px;
    letter-spacing: -0.6px;
  }

  @media (max-width: 800px) {
    width: 100%;
    margin-bottom: 10vw;
    font-size: 30px;
    height: auto;
    top: 68px;
    z-index: 1000;
    background-color: var(--mainBg-color);
  }
}

.about_slide_in_skill {
  width: 1456px;
  margin-left: 100px;

  h5 {
    font-size: 50px;
    margin-top: -35px;
    font-family: 'Noto Serif Display', serif;
  }
  b {
    color: #8ce0ee;
  }
  .skill-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 50px;
    margin: 20px auto 150px;
    width: 100%; /* 너비를 100%로 조정 */
    flex-wrap: wrap;

    li {
      width: 130px;
      height: 130px;
      background: #8ce0ee;
      border-radius: 100px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    img {
      width: 130px;
      height: 75px;
      background: #8ce0ee;
      border: none;
    }

    figure {
      margin-top: 0;
    }
  }
}
</style>
