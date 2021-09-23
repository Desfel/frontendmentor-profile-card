<template>
  <div class="page-wrapper">
    <div class="card-wrapper">
      <div class="card-top">
        <img src="@/assets/img/image-victor.jpg" alt="Victor Crest" />

        <p class="user-name bold-text">
          Victor Crest
          <span>26</span>
        </p>
        <p class="user-city">London</p>
      </div>

      <div class="card-bottom">
        <div class="card-stats">
          <p class="stat-number bold-text">80K</p>
          <p class="stat-type">Followers</p>
        </div>
        <div class="card-stats">
          <p class="stat-number bold-text">803K</p>
          <p class="stat-type">Likes</p>
        </div>
        <div class="card-stats">
          <p class="stat-number bold-text">1.4K</p>
          <p class="stat-type">Photos</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .card-wrapper {
    position: relative;
    display: flex;
    align-items: center;
    flex-direction: column;
    width: 100%;
    max-width: 350px;
    background: $light;
    border-radius: 15px;
    box-shadow: 0 50px 100px -20px rgba(8, 70, 94, 0.504835);
    text-align: center;
  }

  .card-top {
    position: relative;
    width: 100%;
    padding-bottom: 28px;
    background: url('../assets/img/bg-pattern-card.svg') no-repeat;
    background-size: auto 140px;
    border-radius: 15px 15px 0 0;
    border-bottom: 1px solid $borderColor;

    img {
      margin: 87px auto 24px;
      border: 5px solid $light;
      border-radius: 50%;
    }

    .user-name {
      span {
        margin-left: 8px;
        font-weight: 400;
      }
    }

    .user-city {
      margin-top: 10px;
    }
  }

  .card-bottom {
    display: flex;
    align-content: center;
    justify-content: space-between;
    width: 100%;
    padding: 24px 40px;
    text-align: center;

    .card-stats {
      width: calc(100% / 3);
    }

    .stat-type {
      margin-top: 10px;
      font-size: 10px;
      line-height: 10px;
      letter-spacing: 1.5px;
    }
  }
}
</style>
