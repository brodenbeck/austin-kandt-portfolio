<template>
  <section class="dribbble reverse-mobile">
    <div class="wrapper">
      <div class="dribbble__shots order-1">
        <a href="https://dribbble.com/shots/6494831-Daily-UI-001-Signup" target="_blank" class="dribbble__shot">
          <img class="dribbble__shot-image" src="/images/dailyui-001_signup.gif" alt="" />
        </a>
        <a href="https://dribbble.com/shots/6454925-Daily-UI-005-App-Icon" target="_blank" class="dribbble__shot">
          <img class="dribbble__shot-image" src="/images/dailyui-005_appicon.jpg" alt="" />
        </a>
        <a href="https://dribbble.com/shots/5987028-Cozilo-Logo-Options" target="_blank" class="dribbble__shot">
          <img class="dribbble__shot-image" src="/images/cozilo_logooptions.jpg" alt="" />
        </a>
        <a href="https://dribbble.com/shots/5974269-Amtech-Logo-Concept" target="_blank" class="dribbble__shot">
          <img class="dribbble__shot-image" src="/images/amtech_opt1_icon.gif" alt="" />
        </a>
      </div>
      <div class="dribbble__description order-0">
        <dribbble-icon color="#EA4C89" />
        <h2 class="m-top-5 m-bottom-0">Latest Dribbble Shots</h2>
        <a class="project__link" href="https://dribbble.com/austinkandt" target="_blank">
          See more
          <arrow-icon></arrow-icon>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ArrowIcon from './icons/Arrow.vue';
import DribbbleIcon from './icons/Dribbble.vue';

export default {
  name: 'DribbblePosts',
  data() {
    return {};
  },
  components: {
    'arrow-icon': ArrowIcon,
    'dribbble-icon': DribbbleIcon,
  },
};
</script>

<style scoped>
.dribbble {
  background: var(--light-gray);
  padding: 35px 0 40px;
}

.dribbble .wrapper {
  display: flex;
}

.dribbble-icon {
  height: 35px;
  width: 35px;
}

.dribbble__shots {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: space-between;
}

.project__link {
  margin: 0 0 20px;
}

.dribbble__shot {
  border: 6px solid white;
  display: block;
  margin-bottom: 14px;
  width: calc((100% - 14px) / 2);
}

.dribbble__shot-image {
  display: block;
  width: 100%;
}

@media only screen and (max-width: 767px) {
  .dribbble .wrapper {
    flex-direction: column;
  }

  .order-1 {
    order: 1;
  }

  .order-0 {
    order: 0;
  }
}

@media only screen and (min-width: 768px) {
  .dribbble .wrapper {
    flex-direction: row;
    align-items: center;
  }

  .dribbble__shots {
    width: 420px;
    margin-right: 90px;
  }

  .dribbble__shot {
    width: 200px;
  }

  .dribbble__description {
    flex: 1;
  }

  .project__link {
    margin: 10px 0 0;
  }

  .dribbble-icon {
    height: 50px;
    width: 50px;
  }
}

@media only screen and (min-width: 965px) {
  .dribbble__shots {
    margin-right: 150px;
  }
}
</style>
