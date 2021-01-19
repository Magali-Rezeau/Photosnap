<template>
  <section class="plan">
    <div class="plan-header">
      <label
        :for="id + '-button'"
        :class="{ active: isActive }"
        class="toggle-button"
      >
        <span class="toggle-label" :style="isActive ? 'opacity: .6' : 'opacity: 1'">Monthly</span>

        <input
          type="checkbox"
          :disabled="disabled"
          :id="id + '-button'"
          v-model="checkedValue"
        />
        <span class="toggle-switch"></span>
        <span class="toggle-label" :style="!isActive ? 'opacity: .6' : 'opacity: 1'">Yearly</span>
      </label>
    </div>
    <div class="plan-cards">
      <div class="plan-cards-box" v-for="card in cards" :key="card.plan">
        <div class="plan-cards-box-text">
          <h2>{{ card.plan }}</h2>
          <p>{{ card.description }}</p>
        </div>
        <div class="plan-cards-box-price">
          <span v-if="currentState">{{ card.pricePerMonth }}</span>
          <span v-else>{{ card.pricePerYear }}</span>
          <span>{{ billingCycle }}</span>
        </div>
        <button class="btn">Pick plan</button>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      currentState: this.defaultState,
      cards: [
        {
          plan: "Basic",
          description: `Includes basic usage of our platform. Recommended for new and aspiring
          photographers.`,
          pricePerMonth: "$ 19.00",
          pricePerYear: "$ 190.00",
          billingCycle: this.currentState ? "Per month" : "Per year",
        },
        {
          plan: "Pro",
          description: ` More advanced features available. Recommended for photography veterans and professionals.`,
          pricePerMonth: "$ 39.00",
          pricePerYear: "$ 390.00",
          billingCycle: this.currentState ? "Per month" : "Per year",
        },
        {
          plan: "Business",
          description: ` Additional features available such as more detailed metrics. Recommended for business owners.`,
          pricePerMonth: "$ 99.00",
          pricePerYear: "$ 990.00",
          billingCycle: this.currentState ? "Per month" : "Per year",
        },
      ],
    };
  },
  props: {
    disabled: {
      type: Boolean,
      default: false,
    },
    defaultState: {
      type: Boolean,
      default: false,
    },
  },

  computed: {
    isActive() {
      return this.currentState;
    },

    checkedValue: {
      get() {
        return this.currentState;
      },
      set(newValue) {
        this.currentState = newValue;
        this.$emit("change", newValue);
      },
    },
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
.plan {
  &-header {
    width: 16rem;
    margin: 4rem 3.75rem 2.5rem 3.75rem;
    @include sm {
      margin: 7rem 16rem 2.6875rem 16rem;
    }
    @include md {
      margin: 7.5rem auto 3rem auto;
    }
    & .toggle-label {
      display: block;
      font-weight: 700;
      font-size: 18px;
      line-height: 25px;
    }
    & .toggle-button {
      display: flex;
      justify-content: space-between;
      align-items: center;
      cursor: pointer;
      width: 16rem;
      height: 2rem;
      & input[type="checkbox"] {
        opacity: 0;
        position: absolute;
        width: 1px;
        height: 1px;
      }
      & .toggle-switch {
        display: inline-block;
        height: 2rem;
        border-radius: 16px;
        width: 4rem;
        background: black;
        box-shadow: inset 0 0 1px #bfcbd9;
        position: relative;
        margin-left: 10px;
        transition: all 0.25s;
      }

      & .toggle-switch::after,
      & .toggle-switch::before {
        content: "";

        display: block;
        height: 1.5rem;
        width: 1.5rem;
        border-radius: 50%;
        position: absolute;
        left: 54.9%;
        right: 35.69%;
        top: 12.5%;
        bottom: 12.5%;
        transform: translateX(0);
        transition: all 0.25s cubic-bezier(0.5, -0.6, 0.5, 1.6);
      }

      & .toggle-switch::after {
        background: white;
        box-shadow: 0 0 1px #666;
      }

      & .toggle-switch::before {
        background: black;
        box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.1);
        opacity: 0;
      }
    }
    & .active {
      & .toggle-switch {
        background: #d7d7d7;
        box-shadow: inset 0 0 1px #adedcb;
      }
      & .toggle-switch::after,
      & .toggle-switch::before {
        transform: translateX(4rem - 1.5rem);
        background-color: black;
      }
      & .toggle-switch::after {
        left: -54.9%;
      }
    }
  }
  &-cards {
    display: grid;
    grid-template-rows: repeat(3, 25.43rem);
    grid-gap: 1.5rem;
    width: 100%;
    @include sm {
      grid-template-rows: repeat(3, 16.875rem);
    }
    @include md {
      grid-template-columns: repeat(3, 21.875rem);
      grid-template-rows: 29.375rem;
      grid-gap: 1.875rem;
      justify-content: center;
    }

    &-box {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      margin: 0 1.75rem;
      padding: 3.5rem 2.3rem;
      background-color: #f5f5f5;
      transition: all 0.3s;
      @include sm {
        flex-direction: row;
        flex-wrap: wrap;
        align-items: stretch;
        padding: 2.5rem;
      }
      @include md {
        margin: 0;
        flex-direction: column;
        align-items: center;
        padding: 5.81rem 2.5rem 5.5rem 2.5rem;
      }
      &:hover {
        transform: scaleY(1.1);
        cursor: pointer;
      }
      &:nth-child(2) {
        background-color: black;
        color: white;

        & .btn {
          background-color: white;
          color: black;
        }
      }
      &-text {
        @include sm {
          flex-basis: 50%;
          align-self: flex-start;
          height: 7.4rem;
        }
        & h2 {
          font-weight: 700;
          font-size: 24px;
          line-height: 25px;
          margin-bottom: 1.125rem;
          text-align: center;
        }
        & p {
          font-weight: 400;
          font-size: 15px;
          line-height: 25px;
          opacity: 0.6;
          text-align: center;
          @include sm {
            text-align: left;
          }
        }
      }

      &-price {
        @include sm {
          flex-basis: 30%;
        }
        & span {
          display: block;
          &:first-child {
            font-weight: 700;
            font-size: 40px;
            line-height: 48px;
            text-align: center;
            letter-spacing: 4.16667px;
            text-transform: uppercase;
          }
          &:last-child {
            font-weight: 400;
            font-size: 15px;
            line-height: 25px;

            text-align: center;

            opacity: 0.6;
          }
        }
      }
      & .btn {
        width: 15.3rem;
        @include sm {
          align-self: flex-end;
        }
      }
    }
  }
}
</style>
