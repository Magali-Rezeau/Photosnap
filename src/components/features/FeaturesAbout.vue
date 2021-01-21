<template>
  <section class="about">
    <div class="about-box">
      <picture class="about-box-img">
        <source
          media="(min-width: 600px)  and (max-width: 1099px)"
          srcset="./../../assets/img/features/hero-features-tablet.jpg"
        />
        <source
          media="(min-width: 1100px)"
          srcset="./../../assets/img/features/hero-features-desktop.jpg"
        />
        <img src="./../../assets/img/features/hero-features-mobile.jpg" alt="" />
      </picture>
      <div class="about-box-text">
        <h1>Features</h1>
        <p>
          We make sure all of our features are designed to be loved by every aspiring and even professional photograpers who wanted to share their stories.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@mixin sm {
  @media (min-width: 600px) {
    @content;
  }
}
@mixin md {
  @media (min-width: 1100px) {
    @content;
  }
}
.about {
  &-box {
    height: 100%;
    display: grid;
    grid-template-rows: repeat(2, 18.75rem);
  position: relative;
    @include sm {
      grid-template-rows: 100%;
      grid-template-columns: 65% 35%;
    }
    @include md {
      grid-template-columns: 42% 58%;
    }
   
    &::after{
      content: "";
      position: absolute;
      top: 18.75rem;
      left: 2rem;
      width: 8rem;
      height: 0.375rem;
      background: linear-gradient(
        26.57deg,
        #ffc593 0%,
        #bc7198 43.29%,
        #5a77ff 83.33%
      );
      @include sm {
        transform: rotate(90deg);
        width: 9.5rem;
        left: -4.6rem;
        top: 50%;
      }
    }
    &-img {
      overflow: hidden;
    }
    &-text {
      padding: 4.5rem 1.75rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      width: 100%;
      background-color: black;
      @include sm {
        padding: 10rem 3.375rem;
        grid-row: 1 / 2;
        grid-column: 1 / 2;
      }
      @include md {
        padding: 10.81rem 7rem;
      }

      & h1 {
        font-weight: 700;
        font-size: 32px;
        line-height: 40px;
        letter-spacing: 3.33px;
        text-transform: uppercase;
        color: #ffffff;
        text-transform: uppercase;
        @include sm {
          font-size: 40px;
          line-height: 48px;
          letter-spacing: 4.16667px;
        }
      }
      & p {
        font-weight: 400;
        font-size: 15px;
        line-height: 25px;

        color: #ffffff;

        opacity: 0.6;
      }
    }
  }
}
</style>
