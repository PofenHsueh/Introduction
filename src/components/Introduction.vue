<template>
  <div class="h-screen px-6 py-6">
    <div class="text-secondary flex items-center">
      <div class="mr-8">
        <img :src="myself" class="h-48 rounded-full" />
      </div>
      <div>
        <div class="flex my-3" v-for="(item, index) in items" :key="index">
          <i class="material-icons mr-2 text-primary">{{ item.icon }}</i>
          <p class="font-bold">{{ item.value }}</p>
        </div>
      </div>
      <section class="ml-auto self-start mt-3">
        <h3 class="title">學歷</h3>
        <ul>
          <li class="text-sm">
            實踐大學 資訊科技與通訊學系 -<span class="text-xs">2018.06</span>
          </li>
        </ul>
      </section>
      <!-- <section class="ml-auto">
        <h3 class="title">技能</h3>
        <div class="flex items-center">
          <div
            v-for="(skill, index) in skills"
            :key="index"
            class="text-center mx-4 my-4"
          >
            <div
              class="flex flex-col  items-center justify-center h-16 w-16 rounded-md bg-gray-100"
            >
              <img :src="skill.img" class="h-10 rounded-md" />
            </div>
            <p class="text-xs">{{ skill.val }}</p>
          </div>
        </div>
      </section> -->
    </div>
    <a href="https://github.com/PofenHsueh?tab=repositories" target="_blank"
      ><img :src="githubImg" class="h-8 ml-40"
    /></a>
    <hr class="my-2" />
    <section>
      <h3 class="title">經歷</h3>
      <ul>
        <li class="text-sm">
          薩摩亞商百星數位智能股份有限公司台灣分公司 -<span class="text-xs"
            >2019.04 ~至今</span
          >
          <p>
            在公司擔任前端的角色，有2年開發經驗，主要工作為畫面的切版，api的串接以及前端架構之規劃
          </p>
        </li>
      </ul>
    </section>
    <section>
      <h3 class="title">技能</h3>
      <div class="flex items-center">
        <div
          v-for="(skill, index) in skills"
          :key="index"
          class="text-center mx-4 my-4"
        >
          <div
            class="flex flex-col  items-center justify-center h-16 w-16 rounded-md bg-gray-100"
          >
            <img :src="skill.img" class="h-10 rounded-md" />
          </div>
          <p class="text-sm">{{ skill.val }}</p>
        </div>
      </div>
    </section>
    <section>
      <h3 class="title">作品</h3>
      <ul>
        <li>
          <img src="@/assets/img/booking.png" class="h-52" /><a
            href="https://booking-web-app.herokuapp.com/"
            target="_blank"
            class="text-blue-400"
            >booking</a
          >
        </li>
        <li>
          <img src="@/assets/img/animal-crossing.png" class="h-52" />
          <a
            href="https://animal-crossing-web.herokuapp.com/"
            target="_blank"
            class="text-blue-400"
            >animal-crossing</a
          >
        </li>
      </ul>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      myself: require("@/assets/img/myself.jpg"),
      githubImg: require("@/assets/img/github-mark.png"),
      items: [
        { icon: "person", value: "薛博分" },
        { icon: "work", value: "軟體開發工程師" },
        { icon: "location_on", value: "台灣，高雄" },
        { icon: "mail", value: "sty5312@gmail.com" }
      ],
      skills: [
        { img: require("@/assets/img/html.jpeg"), val: "HTML5" },
        { img: require("@/assets/img/css.jpeg"), val: "CSS3" },
        { img: require("@/assets/img/scss.png"), val: "SCSS" },
        { img: require("@/assets/img/javascript.jpg"), val: "JavaScript" },
        { img: require("@/assets/img/vue.png"), val: "Vue.js" },
        { img: require("@/assets/img/vuetify.png"), val: "Vuetify" },
        { img: require("@/assets/img/ant.png"), val: "Ant Design" },
        { img: require("@/assets/img/tailwind.png"), val: "Tailwind" },
        { img: require("@/assets/img/git.png"), val: "Git" }
      ]
    };
  }
};
</script>
