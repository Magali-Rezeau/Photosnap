<template>
  <section class="about">
    <div class="about-box">
      <picture class="about-box-img">
        <source
          media="(min-width: 600px)  and (max-width: 1099px)"
          srcset="./../../assets/img/create-and-share-tablet.jpg"
        />
        <source
          media="(min-width: 1100px)"
          srcset="./../../assets/img/create-and-share-desktop.jpg"
        />
        <img src="./../../assets/img/create-and-share-mobile.jpg" alt="" />
      </picture>
      <div class="about-box-text">
        <h2>Create and share your photo Stories</h2>
        <p>
          Photosnap is a platform for photographers and visual storytellers. We
          make it easy to share photos, tell stories and connect with others.
        </p>
        <div class="about-box-text-link">
          <a>Get an invite</a>
          <button>
            <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
              <g fill="none" fill-rule="evenodd" stroke="#fff">
                <path d="M0 7h41.864M35.428 1l6 6-6 6" />
              </g>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <div class="about-box">
      <picture class="about-box-img">
        <source
          media="(min-width: 700px)  and (max-width: 1099px)"
          srcset="./../../assets/img/beautiful-stories-tablet.jpg"
        />
        <source
          media="(min-width: 1100px)"
          srcset="./../../assets/img/beautiful-stories-desktop.jpg"
        />
        <img src="./../../assets/img/beautiful-stories-mobile.jpg" alt="" />
      </picture>
      <div class="about-box-text">
        <h2>Beautiful stories every time</h2>
        <p>
          We provide design templates to ensure your stories look terrific.
          Easily add photos, text, embed maps and media from other networks.
          Then share your story with everyone.
        </p>
        <div class="about-box-text-link">
          <a>View the stories</a>
          <button>
            <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
              <g fill="none" fill-rule="evenodd" stroke="#000">
                <path d="M0 7h41.864M35.428 1l6 6-6 6" />
              </g>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <div class="about-box">
      <picture class="about-box-img">
        <source
          media="(min-width: 700px) and (max-width: 1099px)"
          srcset="./../../assets/img/designed-for-everyone-tablet.jpg"
        />
        <source
          media="(min-width: 1100px)"
          srcset="./../../assets/img/designed-for-everyone-desktop.jpg"
        />
        <img src="./../../assets/img/designed-for-everyone-mobile.jpg" alt="" />
      </picture>
      <div class="about-box-text">
        <h2>Designed for everyone</h2>
        <p>
          Photosnap can help you create stories that resonate with your
          audience. Our tool is designed for photographers of all levels,
          brands, businesses you name it.
        </p>
        <div class="about-box-text-link">
          <a>View the stories</a>
          <button>
            <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
              <g fill="none" fill-rule="evenodd" stroke="#000">
                <path d="M0 7h41.864M35.428 1l6 6-6 6" />
              </g>
            </svg>
          </button>
        </div>
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
  display: grid;
  grid-template-rows: 43.125rem repeat(2, 44.56rem);

  @include sm {
    grid-template-rows: 40.625rem repeat(2, 37.5rem);
  }

  &-box {
    height: 100%;
    display: grid;
    grid-template-rows: 35% 65%;
    position: relative;
    &:nth-child(1):after {
      content: "";
      position: absolute;
      top: 35%;
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
        width: 19rem;
        left: -9.3rem;
        top: 45%;
      }
    }
    @include sm {
      grid-template-rows: 100%;
      grid-template-columns: 32.5% 32.5% 35%;
    }
    @include md {
      grid-template-rows: 100%;
      grid-template-columns: 40% 20% 40%;
    }
    &:nth-child(1) > picture {
      @include sm {
        grid-row: 1 /2;
        grid-column: 3 /4;
      }
      @include md {
        grid-column: 2 /4;
      }
    }
    &:nth-child(1) > div {
      background-color: black;
      color: white;

      @include sm {
        grid-row: 1 /2;
        grid-column: 1 /3;
      }
      @include md {
        grid-column: 1 /2;
      }
      & a {
        color: white;
      }
    }
    &:nth-child(2) > picture {
      @include sm {
        grid-row: 1 /2;
        grid-column: 1 /2;
      }
      @include md {
        grid-column: 1 /3;
      }
    }
    &:nth-child(2) > div {
      @include sm {
        grid-row: 1 /2;
        grid-column: 2 /4;
      }
      @include md {
        grid-column: 3 /4;
      }
    }
    &:nth-child(3) > picture {
      @include sm {
        grid-column: 3 /4;
      }
      @include md {
        grid-column: 2 /4;
      }
    }
    &:nth-child(3) > div {
      @include sm {
        grid-row: 1 /2;
        grid-column: 1 /3;
      }
      @include md {
        grid-row: 1 /2;
        grid-column: 1 /2;
      }
    }

    &-img {
      overflow: hidden;
    }
    &-text {
      padding: 4.5rem 2rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      width: 100%;
      @include sm {
        padding: 10rem 2.75rem;
      }
      @include md {
        padding: 8.45rem 7rem;
      }

      & h2 {
        font-size: 32px;
        font-weight: 700;
        line-height: 40px;
        letter-spacing: 3.33px;
        text-transform: uppercase;
        @include sm {
          line-height: 48px;

          letter-spacing: 4.16667px;
        }
      }
      & p {
        font-weight: 400;
        font-size: 15px;
        line-height: 25px;
        opacity: 0.6;
      }
      &-link {
        display: flex;
        justify-content: space-between;
        width: 12.81rem;

        & a {
          font-weight: 700;
          font-size: 12px;
          line-height: 16.62px;
          letter-spacing: 2px;
          text-transform: uppercase;
          color: black;

          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
}
</style>
