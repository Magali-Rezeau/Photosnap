<template>
  <section class="about">
    <div class="about-box">
      <figure class="about-box-img">
        <img src="./../assets/img/create-and-share.jpg" alt="" />
      </figure>
      <div class="about-box-text">
        <h2>Create and share your photo Stories</h2>
        <p>
          Photosnap is a platform for photographers and visual storytellers. We
          make it easy to share photos, tell stories and connect with others.
        </p>
        <div class="about-box-text-link">
          <h3>Get an invite</h3>
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
      <figure class="about-box-img">
        <img src="./../assets/img/beautiful-stories.jpg" alt="" />
      </figure>
      <div class="about-box-text">
        <h2>Beautiful stories every time</h2>
        <p>
          We provide design templates to ensure your stories look terrific.
          Easily add photos, text, embed maps and media from other networks.
          Then share your story with everyone.
        </p>
        <div class="about-box-text-link">
          <h3>View the stories</h3>
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
      <figure class="about-box-img">
        <img src="./../assets/img/designed-for-everyone.jpg" alt="" />
      </figure>
      <div class="about-box-text">
        <h2>Designed for everyone</h2>
        <p>
          Photosnap can help you create stories that resonate with your
          audience. Our tool is designed for photographers of all levels,
          brands, businesses you name it.
        </p>
        <div class="about-box-text-link">
          <h3>View the stories</h3>
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
.about {
  display: grid;
  grid-template-rows: 43.125rem repeat(2, 44.56rem);

  &-box {
    height: 100%;
    display: grid;
    grid-template-rows: 40% 60%;
    &:nth-child(1) {
      background-color: black;
      color: white;
    }
    &-text {
      padding: 4.5rem 2rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      & h2 {
        font-size: 32px;
        font-weight: 700;
        line-height: 40px;
        letter-spacing: 3.33px;
        text-transform: uppercase;
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
        & h3 {
          font-weight: 700;
          font-size: 12px;
          line-height: 16.62px;
          letter-spacing: 2px;
          text-transform: uppercase;
        }
      }
    }
  }
}
</style>
