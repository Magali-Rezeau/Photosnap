<template>
<section class="link">
      <h2>We’re in beta. Get your invite today!</h2>
      <div class="link-btn">
        <span>Get an invite</span>
        <button>
          <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
            <g fill="none" fill-rule="evenodd" stroke="#fff">
              <path d="M0 7h41.864M35.428 1l6 6-6 6" />
            </g>
          </svg>
        </button>
      </div>
    </section>
</template>

<script>
export default {};
</script>

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
 .link {
    height: 18rem;
    background-image: url("./../assets/img/pricing/bg-beta-mobile.jpg");
    padding: 0 2.5rem;
    position: relative;
    @include sm {
      background-image: url("./../assets/img/pricing/bg-beta-tablet.jpg");
      height: 17.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    @include md {
      background-image: url("./../assets/img/pricing/bg-beta-desktop.jpg");
      padding: 0 10rem;
    }
    &::before {
      content: "";
      position: absolute;
      top: 0;
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
        width: 17.5rem;
        left: -8.6rem;
        top: 49%;
      }
    }
    & h2 {
      padding-top: 4rem;
      font-weight: 700;
      font-size: 32px;
      line-height: 40px;
      letter-spacing: 3.33333px;
      text-transform: uppercase;
      color: white;
      @include sm {
        padding-top: 0;
        width: 25rem;
        font-size: 40px;
        line-height: 48px;
        letter-spacing: 4.16667px;
      }
    }
    &-btn {
      font-weight: 700;
      font-size: 12px;
      line-height: 16px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: white;
      width: 10.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 1.5rem;
      @include sm {
        margin-top: 0;
      }
    }
  }
</style>
