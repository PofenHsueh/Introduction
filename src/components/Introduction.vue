<template>
  <div class="h-screen px-6 py-6">
    <div class="text-secondary flex items-center">
      <div class="mr-8">
        <img src="@/assets/img/myself.jpg" class="h-48 rounded-full" />
      </div>
      <div>
        <div class="flex my-3" v-for="(item,index) in items" :key="index">
            <i class="material-icons mr-2 text-primary">{{item.icon}}</i>
            <p class="font-bold">{{item.value}}</p>
        </div>
      </div>
      <section>
          <h3 class="bg-primary text-white text-xl px-2 py-1 rounded-md">技能</h3>
       <ul>
           <li></li>
       </ul>
      </section>
    </div>
    <a href="https://github.com/PofenHsueh?tab=repositories" target="_blank"><img src="@/assets/img/github-mark.png"  class="h-8 ml-40"/></a>
    <hr class="my-2"/>
  </div>
</template>
<script>
export default {
    data(){
        return{
            items:[{icon:"person",value:"薛博分"},{icon:"work",value:"軟體開發工程師"},{icon:"location_on",value:"台灣，高雄"},{icon:"mail",value:"sty5312@gmail.com"}]
        }
    }
};
</script>
