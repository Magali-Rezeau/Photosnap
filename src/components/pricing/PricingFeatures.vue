<template>
  <section class="features">
    <h1>Compare</h1>
    <div class="features-table">
      <div class="features-table-heading">
        <h3>The features</h3>
        <ul class="features-table-heading-list">
          <li class="features-table-heading-list-item">Basic</li>
          <li class="features-table-heading-list-item">Pro</li>
          <li class="features-table-heading-list-item">Business</li>
        </ul>
        <hr />
      </div>
      <div
        class="features-table-details"
        v-for="feature in features"
        :key="feature.name"
      >
        <div class="features-table-details-header">
          <h3>{{ feature.name }}</h3>
        </div>
        <ul class="features-table-details-list">
          <li class="features-table-details-list-item">
            <span>Basic</span>
            <svg
              v-if="feature.basic"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="15"
            >
              <path
                fill="none"
                stroke="#000"
                stroke-width="2"
                d="M1 8.124L5.623 13 17 1"
              />
            </svg>
          </li>
          <li class="features-table-details-list-item">
            <span>Pro</span>
            <svg
              v-if="feature.pro"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="15"
            >
              <path
                fill="none"
                stroke="#000"
                stroke-width="2"
                d="M1 8.124L5.623 13 17 1"
              />
            </svg>
          </li>
          <li class="features-table-details-list-item">
            <span>Business</span>
            <svg
              v-if="feature.business"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="15"
            >
              <path
                fill="none"
                stroke="#000"
                stroke-width="2"
                d="M1 8.124L5.623 13 17 1"
              />
            </svg>
          </li>
        </ul>
        <hr />
      </div>
    </div>
    <app-link></app-link>
  </section>
</template>
<script>
import AppLink from './../AppLink.vue';
export default {
  components: {
    AppLink,
  },
  data() {
    return {
      features: [
        {
          name: "Unlimited Story Posting",
          basic: true,
          pro: true,
          business: true,
        },
        {
          name: "Unlimited Photo Upload",
          basic: true,
          pro: true,
          business: true,
        },
        {
          name: "Embedding Custom Content",
          basic: false,
          pro: true,
          business: true,
        },
        {
          name: "Customize Metadata",
          basic: false,
          pro: true,
          business: true,
        },
        {
          name: "Advanced Metrics",
          basic: false,
          pro: false,
          business: true,
        },
        {
          name: "Photo Downloads",
          basic: false,
          pro: false,
          business: true,
        },
        {
          name: "Search Engine Indexing",
          basic: false,
          pro: false,
          business: true,
        },
        {
          name: "Custom Analytics",
          basic: false,
          pro: false,
          business: true,
        },
      ],
    };
  },
};
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
.features {
 
  width: 100%;
  & h1 {
    display: none;
     font-weight: bold;
font-size: 40px;
line-height: 48px;

text-align: center;
letter-spacing: 4.16667px;
text-transform: uppercase;
margin: 10rem auto 3.5rem auto;
    @include md {
      display: block;

    }
   
  }
  &-table {
    padding: 3.5rem 2.3rem;
    @include md {
      width: 45.6875rem;
      margin: 0 auto;
      padding: 0 0 10rem 0;
    }
    &-heading {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      width: 100%;
      & h3 {
        font-weight: 700;
        font-size: 12px;
        line-height: 16px;
        letter-spacing: 2px;

        @include sm {
          width: 50%;
        }
      }
      & hr {
        margin: 1.4375rem 0;
        height: 0.0625rem;
        width: 100%;
        display: block;
      }
      &-list {
        display: none;
        @include sm {
          justify-self: flex-end;
          display: flex;
          justify-content: space-between;
          width: 50%;
        }

        &-item {
          font-weight: 700;
          font-size: 12px;
          line-height: 16px;
          /* identical to box height */

          text-align: center;
          letter-spacing: 2px;
        }
      }
    }
    &-details {
      display: flex;
      flex-wrap: wrap;
      @include sm {
      }
      &-header {
        width: 100%;
        margin-bottom: 1rem;

        font-weight: 700;
        font-size: 12px;
        line-height: 16px;

        letter-spacing: 2px;
        text-transform: uppercase;
        @include sm {
          width: 50%;
          margin: 0;
        }
      }
      &-list {
        display: flex;
        justify-content: space-between;
        width: 100%;
        @include sm {
          display: flex;
          width: 50%;
        }
        &-item {
          @include sm {
            flex-basis: 20%;
          }
          & span {
            display: block;
            font-weight: 700;
            font-size: 10px;
            line-height: 13px;
            letter-spacing: 1.66667px;
            color: #000000;
            opacity: 0.5;
            margin-bottom: 0.125rem;

            @include sm {
              display: none;
            }
          }
          & svg {
            margin-top: 0.5rem;
          }
        }
      }
      & hr {
        margin: 1.5rem 0;
        height: 0.0625rem;
        width: 100%;
        display: block;
        color: #d7d7d7;
      }
    }
  }
}
</style>
