<template>
  <section class="portfolio-intro">
    <h2 class="portfolio-intro__heading">Works</h2>
  </section>
</template>

<style lang="scss" scoped>
@mixin bp-phone {
  @media only screen and (max-width: 599px) {
    @content;
  }
}
@mixin bp-tablet-p {
  @media only screen and (max-width: 899px) and (min-width: 600px) {
    @content;
  }
}
@mixin bp-tablet-l {
  @media only screen and (max-width: 1199px) and (min-width: 900px) {
    @content;
  }
}
@mixin bp-laptop {
  @media only screen and (max-width: 1799px) and (min-width: 1200px) {
    @content;
  }
}
@mixin bp-desktop {
  @media only screen and (min-width: 1800px) {
    @content;
  }
}
@mixin center {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  align-content: center;
}
@mixin center-h {
  text-align: center;
}
@mixin uppercase {
  text-transform: uppercase;
}
@mixin slant {
  transform: skewY(-8deg);
}
@mixin unslant {
  transform: skewY(7deg);
}
@mixin img-left {
  @include slant;
  height: 110vmin;
  width: 100%;
  padding: 1rem;
  display: grid;
  grid-template-columns: 60% 40%;
  grid-template-areas: "img text";
  @include bp-phone {
    height: 77vh;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }
}
@mixin img-right {
  @include slant;
  height: 110vh;
  width: 100%;
  padding: 1rem;
  display: grid;
  grid-template-columns: 40% 60%;
  grid-template-areas: "text img";
  @include bp-phone {
    height: 77vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
}
@mixin grid {
  height: 80vh;
  width: 100%;
  @include slant;
  background-color: transparent;
  margin: 3vh 0;
  display: grid;
  grid-gap: 3vh;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(3, 1fr);
  @include bp-phone {
    height: 40vh;
  }
}
@mixin grid-itm {
  height: 100%;
  width: 100%;
  background-color: var(--primary);
}
@mixin icon {
  font-size: 6vh;
  @include bp-phone {
    font-size: 6vh;
  }
}

@mixin img-left {
  @include slant;
  height: 110vmin;
  width: 100%;
  padding: 1rem;
  display: grid;
  grid-template-columns: 60% 40%;
  grid-template-areas: "img text";
  @include bp-phone {
    height: 77vh;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }
}

.portfolio-intro {
  @include slant;
  height: 25vmin;
  width: 100%;
  padding-top: 3rem;
  background-color: var(--white);
  margin-bottom: -1vmin;
  @include center;
  @include bp-phone {
    height: 77vh;
  }
  &__heading {
    @include uppercase;
    @include unslant;
    letter-spacing: 1.5rem;
    font-size: 13vmin;
    font-weight: bolder;
    color: var(-black);
    @include center-h;
    display: block;
  }
}
</style>
