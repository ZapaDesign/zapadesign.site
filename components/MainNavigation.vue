<template>
  <nav id="nav" class="mainNavigation">
    <nuxt-link to="/about" class="logo">
      <img alt="ZapaDesign Logo" src="~/assets/logo.svg" />
    </nuxt-link>

    <nuxt-link to="/">
      <div>{{ $t('links.home') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_services"></use>
        </svg>
      </div>
    </nuxt-link>

    <nuxt-link to="/about">
      <div>{{ $t('links.about') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_about"></use>
        </svg>
      </div>
    </nuxt-link>

    <nuxt-link to="/skills">
      <div>{{ $t('links.skills') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_skills"></use>
        </svg>
      </div>
    </nuxt-link>

    <nuxt-link to="/portfolio">
      <div>{{ $t('links.portfolio') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_portfolio"></use>
        </svg>
      </div>
    </nuxt-link>
    <!-- 
    <nuxt-link :to="'/' + $i18n.locale + '/wprocess'">
      <div>{{ $t('links.wprocess') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_wprocess"></use>
        </svg>
      </div>
    </nuxt-link> -->

    <nuxt-link to="/blog">
      <div>{{ $t('links.blog') }}</div>
      <div>
        <svg>
          <use xlink:href="../assets/icons.svg#icon_blog"></use>
        </svg>
      </div>
    </nuxt-link>
  </nav>
</template>

<script>
export default {
  name: 'MainVavigation',
}
</script>

<style lang="scss">
.mainNavigation {
  text-align-last: left;
  text-align: left;
  a {
    display: flex;
    justify-content: space-between;
    margin: 3% 0;
    font-family: $opxc;
    font-size: 1rem;
    font-weight: 400;
    letter-spacing: 0.125em;
    color: #ddd;
    text-decoration: none;
    div:first-child {
      flex: 1;
      padding: 3% 0 3% 10%;
      background-image: linear-gradient(
        to left,
        transparent,
        transparent 50%,
        #3d3d3d 50%,
        #3d3d3d
      );
      background-position: 100% 0;
      background-size: 200% 100%;
      transition: all 1s ease-in;
      position: relative;
      &:after {
        content: '';
        height: 1px;
        width: 0px;
        display: block;
        background-color: $acf;
        transition: all 1s ease-in;
        transform: rotate(180deg);
        position: absolute;
        right: 0;
        bottom: 5px;
      }
    }
    div:last-child {
      width: 50px;
    }
    &.nuxt-link-exact-active {
      // color: #42b983;
      background-position: 0 0;
      svg {
        fill: $acf;
      }
      div:first-child {
        background-position: 0 0;
        background-size: 200% 100%;
        &:after {
          content: '';
          width: 65%;
        }
      }
    }
    @media (min-width: 720px) and (max-width: 960px) {
      & {
        letter-spacing: 0.05em;
      }
    }
    @media (min-width: 960px) {
      font-size: 1.125rem;
      letter-spacing: 0.15em;
    }
    // &:hover {
    //   // color: $acf;
    // }
  }
  a:first-child {
    margin: 0;
  }

  svg {
    position: relative;
    top: 25%;
    display: block;
    margin: 0 auto;
    width: 16px;
    height: 16px;
    fill: $sbic;
  }
}

.logo {
  padding: 5% 0;
  img {
    width: 100%;
    height: 100%;
  }
}
</style>
