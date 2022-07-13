<template>
  <div class="tech">
    <my-title title="Technologies we work with" />
    <div class="tech__block">
      <router-link
        v-motion-pop-visible
        to="/"
        class="tech__item"
        v-for="t in tech"
        :key="t.id"
      >
        <img class="tech__svg" :src="t.src" :alt="t.text" />
        <div class="tech__title">{{ t.text }}</div>
        <div class="tech__text">
          {{ t.description }}
        </div>
      </router-link>
    </div>
  </div>
</template>

<script setup>
import MyTitle from "./MyTitle.vue";
import react from "../assets/images/icon/react.svg";
import angular from "../assets/images/icon/angular.svg";
import vue from "../assets/images/icon/vue.svg";
import c from "../assets/images/icon/c.svg";
import flutter from "../assets/images/icon/flutter.svg";
import python from "../assets/images/icon/python.svg";
import swift from "../assets/images/icon/swift.svg";
import java from "../assets/images/icon/java.svg";

const tech = [
  {
    id: 1,
    text: "react",
    src: react,
    description:
      "React is developed and maintained by Facebook, Instagram, and a community of individual developers and corporations. React can be used to develop single page and mobile applications. Its goal is to provide high development speed, simplicity and scalability. As a library for developing user interfaces, React is often used with other libraries.",
  },
  {
    id: 2,
    text: "angular",
    src: angular,
    description:
      "An open and free platform for developing web applications written in TypeScript, developed by a team from Google, as well as a community of developers from various companies. Angular is a completely rewritten framework from the same team that wrote AngularJS.",
  },
  {
    id: 3,
    text: "vue",
    src: vue,
    description:
      " It can function as a web framework for developing single-page applications in a reactive style.Currently maintained by creator Evan Yu and the rest of the active core team members from various companies such as Netlify, Netguru, Baidu, Livestorm. A 2016 survey for JavaScript found Vue to have 89% developer satisfaction. On GitHub, the project has 188K stars, is the third largest project in the history of GitHub",
  },
  {
    id: 4,
    text: "c++",
    src: c,
    description:
      "Compiled, statically typed general-purpose programming language. Supports such programming paradigms as procedural programming, object-oriented programming, generic programming.",
  },
  {
    id: 5,
    text: "flutter",
    src: flutter,
    description:
      "An open source development kit and framework for creating mobile applications for Android and iOS, web applications, and desktop applications for Windows, macOS and Linux using the Dart programming language, developed and developed by Google Corporation.",
  },
  {
    id: 6,
    text: "java",
    src: java,
    description:
      "A strongly typed general-purpose object-oriented programming language developed by Sun Microsystems (later acquired by Oracle). Development is driven by a community organized through the Java Community Process; the language and the main technologies that implement it are distributed under the GPL license. Trademark rights are owned by Oracle Corporation.",
  },
  {
    id: 7,
    text: "swift",
    src: swift,
    description:
      "An open multi-paradigm general-purpose compiled programming language developed and maintained by Apple. The first version was introduced in 2014. Swift is most commonly used in app development for macOS, iOS, iPadOS, watchOS, and tvOS, but the language is also available for Windows and Linux.",
  },
  {
    id: 8,
    text: "python",
    src: python,
    description:
      "A high-level, general-purpose programming language with dynamic strong typing and automatic memory management, focused on improving developer productivity, code readability and quality, and ensuring the portability of programs written in it. The language is completely object-oriented in the sense that everything is an object.",
  },
];
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins.scss";

.tech {
  @include fluid(margin-bottom, 25px, 50px);
  @include container;

  &__block {
    display: flex;
    flex-wrap: wrap;
  }

  &__item {
    @include fluid(padding-top, 20px, 40px);
    @include fluid(padding-bottom, 20px, 40px);
    @include fluid(padding-right, 20px, 40px);
    @include fluid(padding-left, 20px, 40px);
    transition: $trn;
    border-radius: 15px;
    width: 20%;
    margin-right: 6.6%;
    margin-bottom: 5%;
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid $light;

    &:nth-child(4n) {
      margin-right: 0;
    }

    &:hover {
      @include hover;

      .tech {
        &__svg {
          opacity: 1;
        }
      }
    }
  }

  &__svg {
    @include fluid(width, 50px, 60px);
    @include fluid(height, 50px, 60px);
    @include fluid(margin-bottom, 10px, 20px);
    transition: $trn;
    opacity: 0.8;
    object-fit: contain;
  }

  &__title {
    @include fluid(font-size, 14px, 18px);
    @include fluid(margin-bottom, 10px, 20px);
    color: #fff;
    text-transform: uppercase;
    font-weight: 600;
  }

  &__text {
    text-align: center;
  }
}

@media screen and (max-width: 992px) {
  .tech {
    &__block {
      justify-content: space-between;
    }

    &__item {
      width: 49%;
      margin-right: 0;
      margin-bottom: 2%;
    }
  }
}

@media screen and (max-width: 576px) {
  .tech {
    &__item {
      width: 100%;
      margin-bottom: 30px;
    }
  }
}
</style>
