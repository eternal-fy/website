<template>
  <div class="about">
    <el-header
      ><h1>
        数计学院算法协会
        <el-select v-model="itemName">
          <el-option
            v-for="(item, index) in site"
            :key="index"
            :value="item"
            :label="item"
          ></el-option>
        </el-select></h1
    ></el-header>
    <div class="textCommonent">
      <div v-if="itemName == '协会简介'">
        <h3>{{ itemName }}</h3>
        <h4>
          <pre class="content">
            算法协会是一个以计算机软件算法为核心的组织，
            它力求以严格、规范、先进的模式，为广大学生提供一个学习、监督、交流的平台，
            为培养专业、全面、领先的计算机高技术型人才服务。
          </pre>
        </h4>
      </div>
      <div v-else-if="itemName == '协会负责人'">
        <h3>{{ itemName }}</h3>
        <h4>
          <pre class="content">
          刘德，男，软工1804班，算法协会会长，入党积极分子。热爱运动，喜欢打羽毛球和乒乓球。为人比较活跃，喜欢参加各种活动，以此来充实自己的大学生活。希望在数计学院算法协会学习到更多专业技能，希望能为数计学院学风建设做出一点贡献。

          杨宇千，男，大类1901班，算法协会副会长。热爱编程，喜欢钻研各种问题，学习最前沿的技术。在GitHub上有着十几万的代码量，拥有一定的开发经验。曾参与过数计学院的网站建设。平时爱好是听音乐，看书。希望能够通过算法协会，为学院的学风和技术氛围的建设做出自己的贡献。
          
          周云，男，软工1801班，算法协会副会长，入党积极分子。兴趣爱好是跑步，打羽毛球，看动漫。专业基础知识掌握牢固，面对困难乐观积极进取，能主动探索自己的知识盲区，拓宽自己的眼界。希望在数计学院算法协会不仅能学习各种优化算法，提升自己的编程能力，更能在与协会成员磨合过程中，提升自己的团队协作能力。
        </pre
          >
        </h4>
      </div>
      <div v-else-if="itemName == '协会机构'">
        <h3>{{ itemName }}</h3>
      </div>
      <div v-else-if="itemName == '协会章程'">
        <h3>{{ itemName }}</h3>
        <h4>
          <pre class="content">
            制定管理制度：协会的正常运行和发展离不开完善的规章制度。目前协会刚刚起步，针对协会当前运营及工作情况，主要对协会成员日常题目训练，题目讲解以及参加会议情况等进行考察并制定相关的管理制度。
            算法协会管理组将主要负责对协会成员日常活动的考察，并建立完善相关制度。
            目前协会主要分为管理组，运行组和宣传组，实行分组管理，各尽其责。同时针对每一位低年级同学，都有一位高年级同学与之对接，即采用一对一方式进行指导和管理。
            根据目前协会运营管理状况，制定如下管理制度：
            （1）每位成员对于平时的做题训练，题目讲解以及开会等活动，不得无故缺勤。若无故缺勤，事后需向管理组负责人阐明具体情况。
            （2）协会成员因紧急的事情而耽误协会工作时，需向相对应负责人请假，阐述具体原因，再由相关负责人向管理组报备，做好记载。
            （3）协会成员不得多次请假，滞后协会工作和日常学习进度，对于多次请假者，需向管理组相关负责人提交一份说明书，要阐明每次缺勤缘由并将耽误的工作弥补起来。
            （4）每位成员在加入协会之前应写一份保证书，表明自己加入协会的意愿并且将为协会的运营建设出力，不能中途退出，否则需向协会负责人分别提交一份退会申请书。
            （5）针对每位成员的平时表现，对于平时表现优异的同学给予适当的奖励（物质奖励和精神奖励）。
            由于协会仍在不断建设之中，各项制度措施会不断完善，我们会在不断摸索中建立健全各项制度。
          </pre>
        </h4>
      </div>
      <div v-else-if="itemName == '联系我们'">
        <h3>{{ itemName }}</h3>
      </div>
      <div v-else-if="itemName == '成员风采'">
        <h3>{{ itemName }}</h3>
      </div>
      <div v-else-if="itemName == '招新专区'">
        <h3>{{ itemName }}</h3>
      </div>
      <div v-else-if="itemName == '技术专栏'">
        <h3>{{ itemName }}</h3>
      </div>
      <div v-else>
        <h3>{{ itemName }}</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      site: [
        "协会简介",
        "协会负责人",
        "协会机构",
        "协会章程",
        "联系我们",
        "成员风采",
        "招新专区",
        "技术专栏",
        "活动纪实",
      ],
      itemName: "协会简介",
    };
  },
};
</script>

<style scoped>
el-header {
  flex-direction: row;
}
.textCommonent {
  margin-top: 50px;
}
.content {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 16px;
  text-align: left;
  white-space: pre-wrap;
  word-wrap: break-word;
  overflow-x: hidden;
}
</style>
