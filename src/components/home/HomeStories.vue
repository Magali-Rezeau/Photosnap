<template>
  <section class="stories">
    <div class="stories-box">
      <figure class="stories-box-figure">
        <picture>
          <source
            media="(min-width: 600px)"
            srcset="./../../assets/img/mountains.jpg"
          />
          <img src="./../../assets/img/mountains-mobile.jpg" alt="mountains" />
        </picture>

        <figcaption class="stories-box-figure-caption">
          <h3>The Mountains</h3>
          <h4>by John Appleseed</h4>
          <hr />
          <div class="stories-box-figure-caption-link">
            <p>Read Story</p>
            <button>
              <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
                <g fill="none" fill-rule="evenodd" stroke="#fff">
                  <path d="M0 7h41.864M35.428 1l6 6-6 6" />
                </g>
              </svg>
            </button>
          </div>
        </figcaption>
      </figure>
    </div>
    <div class="stories-box">
      <figure class="stories-box-figure">
        <picture>
          <source
            media="(min-width: 470px)"
            srcset="./../../assets/img/cityscapes.jpg"
          />
          <img src="./../../assets/img/cityscapes-mobile.jpg" alt="cityscapes" />
        </picture>

        <figcaption class="stories-box-figure-caption">
          <h3>Sunset Cityscapes</h3>
          <h4>by Benjamin Cruz</h4>
          <hr />
          <div class="stories-box-figure-caption-link">
            <p>Read Story</p>
            <button>
              <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
                <g fill="none" fill-rule="evenodd" stroke="#fff">
                  <path d="M0 7h41.864M35.428 1l6 6-6 6" />
                </g>
              </svg>
            </button>
          </div>
        </figcaption>
      </figure>
    </div>
    <div class="stories-box">
      <figure class="stories-box-figure">
        <picture>
          <source
            media="(min-width: 600px)"
            srcset="./../../assets/img/18-days-voyage.jpg"
          />
          <img
            src="./../../assets/img/18-days-voyage-mobile.jpg"
            alt="18-days-voyage"
          />
        </picture>

        <figcaption class="stories-box-figure-caption">
          <h3>18 Days Voyage</h3>
          <h4>by Alexei Borodin</h4>
          <hr />
          <div class="stories-box-figure-caption-link">
            <p>Read Story</p>
            <button>
              <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
                <g fill="none" fill-rule="evenodd" stroke="#fff">
                  <path d="M0 7h41.864M35.428 1l6 6-6 6" />
                </g>
              </svg>
            </button>
          </div>
        </figcaption>
      </figure>
    </div>
    <div class="stories-box">
      <figure class="stories-box-figure">
        <picture>
          <source
            media="(min-width: 600px)"
            srcset="./../../assets/img/architecturals.jpg"
          />
          <img
            src="./../../assets/img/architecturals-mobile.jpg"
            alt="architecturals"
          />
        </picture>

        <figcaption class="stories-box-figure-caption">
          <h3>Architecturals</h3>
          <h4>by Samantha Brooke</h4>
          <hr />
          <div class="stories-box-figure-caption-link">
            <p>Read Story</p>
            <button>
              <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
                <g fill="none" fill-rule="evenodd" stroke="#fff">
                  <path d="M0 7h41.864M35.428 1l6 6-6 6" />
                </g>
              </svg>
            </button>
          </div>
        </figcaption>
      </figure>
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
.stories {
  display: grid;
  grid-template-rows: repeat(4, 23.43rem);
  @include sm {
    grid-template-rows: repeat(2, 31.25rem);
    grid-template-columns: repeat(2, 1fr);
  }
  @include md {
    grid-template-rows: 100%;
    grid-template-columns: repeat(4, 1fr);
  }
  &-box {
    height: 100%;
    position: relative;
    &:hover {
      transform: translateY(-1.5rem);
       &::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 0.375rem;
        background: linear-gradient(
          26.57deg,
          #ffc593 0%,
          #bc7198 43.29%,
          #5a77ff 83.33%
        );
      }
    }
    &-figure {
      position: relative;
      color: white;

      &-caption {
        position: absolute;
        bottom: 2.5rem;
        left: 2rem;
        text-align: left;
        & h3 {
          font-size: 18px;
          line-height: 25px;
          font-weight: 700;
        }
        & h4 {
          font-size: 13px;
          line-height: 16.93px;
          font-weight: 400;
        }
        & hr {
          width: 19.375rem;
          height: 0.0625rem;
          background-color: white;
          opacity: 0.25;
          margin-top: 1rem;
          margin-bottom: 1.25rem;
        }
        &-link {
          display: flex;
          justify-content: space-between;
          & p {
            font-size: 12px;
            line-height: 15.62px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
          }
        }
      }
    }
  }
}
</style>
