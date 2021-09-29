
<template>
  <div id="app">
 
    <div class="loading-class" v-show="page == -1">
      <div class="content-class">
        <img src="./assets/logo-twt.png" style="width: 125px; height: 20px" />
        <vm-progress :percentage="percent"></vm-progress>
      </div>
    </div>
    <div class="cover-class" v-show="page == 0">
      <div class="start-class" @click="start"></div>
      
    </div>
    <div class="q-class" v-show="page == 1">
      <div class="q1-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 2">
      <div class="q1-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 3">
      <div class="q2-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 4">
      <div class="q2-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 5">
      <div class="q3-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 6">
      <div class="q3-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 7">
      <div class="q4-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 8">
      <div class="q4-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 9">
      <div class="q5-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 10">
      <div class="q5-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 11">
      <div class="q6-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 12">
      <div class="q6-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
<div class="q-class" v-show="page == 13">
      <div class="q7-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 14">
      <div class="q7-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
<div class="q-class" v-show="page == 15">
      <div class="q8-1-class">
        <div :class="[qa ? ' qa' : '']"></div>
        <div :class="[qb ? ' qb' : '']"></div>
        <div :class="[qc ? ' qc' : '']"></div>
        <div :class="[qd ? ' qd' : '']"></div>
        <div class="q-a-class" @click="pushChoiceA()"></div>
        <div class="q-b-class" @click="pushChoiceB()"></div>
        <div class="q-c-class" @click="pushChoiceC()"></div>
        <div class="q-d-class" @click="pushChoiceD()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 16">
      <div class="q8-2-class">
          <div class="nextPage" @click="nextPage()"></div>
      </div>
    </div>
    <div class="q-class" v-show="page == 17">
      <div class="memory-class">
        <swiper ref="mySwiper" :options="swiperOptions" class="Swiper">
          <swiper-slide><div class="img1" @click="img(1)"></div></swiper-slide>
          <swiper-slide><div class="img2" @click="img(2)"></div></swiper-slide>
          <swiper-slide><div class="img3" @click="img(3)"></div></swiper-slide>
          <swiper-slide><div class="img4" @click="img(4)"></div></swiper-slide>
          <swiper-slide><div class="img5" @click="img(5)"></div></swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
          </swiper>
         <textarea cols="10" class="textarea" v-model="text" placeholder="点此写下感悟并选择图片以继续" ></textarea>
      </div>
    </div>
    <div class="q-class" v-show="page == 18">
      <div class="q-class" id="captureId1">
        <div class="lastpage1">
          <img src="@/assets/lastPage.png" height="100%" width="100%">
          <div :class="['list1-class' + (statue ? ' list1move' : '')]"><img src="@/assets/list1.png" height="100%" width="100%"></div>
          <div :class="['list2-class' + (statue ? ' list2move' : '')]"><img src="@/assets/list2.png" height="100%" width="100%"></div>
          <div :class="['list3-class' + (statue ? ' list3move' : '')]"><img src="@/assets/list3.png" height="100%" width="100%"></div>
          <div :class="['list4-class' + (statue ? ' list4move' : '')]"><img src="@/assets/list4.png" height="100%" width="100%"></div>
          <div :class="['list5-class' + (statue ? ' list5move' : '')]"><img src="@/assets/list5.png" height="100%" width="100%"></div>
          <div :class="['list6-class' + (statue ? ' list6move' : '')]"><img src="@/assets/list6.png" height="100%" width="100%"></div>
          <div :class="['list7-class' + (statue ? ' list7move' : '')]"><img src="@/assets/list7.png" height="100%" width="100%"></div>
          <div :class="['list8-class' + (statue ? ' list8move' : '')]"><img src="@/assets/list8.png" height="100%" width="100%"></div>
          <div class="iimg1"><img src="@/assets/img1.png" height="100%" width="100%"></div>
          <div class="iiimg1"><img src="@/assets/shitang.png" height="100%" width="100%"></div>
           <div class="text">{{ text }}</div>
        </div>
      </div>
    </div>
    <div class="q-class" v-show="page == 19">
      <div class="q-class" id="captureId2">
        <div class="lastpage2">
          <img src="@/assets/lastPage.png" height="100%" width="100%">
          <div :class="['list1-class' + (statue ? ' list1move' : '')]"><img src="@/assets/list1.png" height="100%" width="100%"></div>
          <div :class="['list2-class' + (statue ? ' list2move' : '')]"><img src="@/assets/list2.png" height="100%" width="100%"></div>
          <div :class="['list3-class' + (statue ? ' list3move' : '')]"><img src="@/assets/list3.png" height="100%" width="100%"></div>
          <div :class="['list4-class' + (statue ? ' list4move' : '')]"><img src="@/assets/list4.png" height="100%" width="100%"></div>
          <div :class="['list5-class' + (statue ? ' list5move' : '')]"><img src="@/assets/list5.png" height="100%" width="100%"></div>
          <div :class="['list6-class' + (statue ? ' list6move' : '')]"><img src="@/assets/list6.png" height="100%" width="100%"></div>
          <div :class="['list7-class' + (statue ? ' list7move' : '')]"><img src="@/assets/list7.png" height="100%" width="100%"></div>
          <div :class="['list8-class' + (statue ? ' list8move' : '')]"><img src="@/assets/list8.png" height="100%" width="100%"></div>
          <div class="iimg2"><img src="@/assets/img2.png" height="100%" width="100%"></div>
          <div class="iiimg2"><img src="@/assets/fensi.png" height="100%" width="100%"></div>
          <div class="text">{{ text }}</div>
        </div>
        </div>
    </div>
    <div class="q-class" v-show="page == 20">
      <div class="q-class" id="captureId3">
        <div class="lastpage3">
          <img src="@/assets/lastPage.png" height="100%" width="100%">
          <div :class="['list1-class' + (statue ? ' list1move' : '')]"><img src="@/assets/list1.png" height="100%" width="100%"></div>
          <div :class="['list2-class' + (statue ? ' list2move' : '')]"><img src="@/assets/list2.png" height="100%" width="100%"></div>
          <div :class="['list3-class' + (statue ? ' list3move' : '')]"><img src="@/assets/list3.png" height="100%" width="100%"></div>
          <div :class="['list4-class' + (statue ? ' list4move' : '')]"><img src="@/assets/list4.png" height="100%" width="100%"></div>
          <div :class="['list5-class' + (statue ? ' list5move' : '')]"><img src="@/assets/list5.png" height="100%" width="100%"></div>
          <div :class="['list6-class' + (statue ? ' list6move' : '')]"><img src="@/assets/list6.png" height="100%" width="100%"></div>
          <div :class="['list7-class' + (statue ? ' list7move' : '')]"><img src="@/assets/list7.png" height="100%" width="100%"></div>
          <div :class="['list8-class' + (statue ? ' list8move' : '')]"><img src="@/assets/list8.png" height="100%" width="100%"></div>
          <div class="iimg3"><img src="@/assets/img3.png" height="100%" width="100%"></div>
          <div class="iiimg3"><img src="@/assets/xuezi.png" height="100%" width="100%"></div>
          <div class="text">{{ text }}</div>
        </div>
      </div>
    </div>
    <div class="q-class" v-show="page == 21">
      <div class="q-class" id="captureId4">
        <div class="lastpage4">
          <img src="@/assets/lastPage.png" height="100%" width="100%">
          <div :class="['list1-class' + (statue ? ' list1move' : '')]"><img src="@/assets/list1.png" height="100%" width="100%"></div>
          <div :class="['list2-class' + (statue ? ' list2move' : '')]"><img src="@/assets/list2.png" height="100%" width="100%"></div>
          <div :class="['list3-class' + (statue ? ' list3move' : '')]"><img src="@/assets/list3.png" height="100%" width="100%"></div>
          <div :class="['list4-class' + (statue ? ' list4move' : '')]"><img src="@/assets/list4.png" height="100%" width="100%"></div>
          <div :class="['list5-class' + (statue ? ' list5move' : '')]"><img src="@/assets/list5.png" height="100%" width="100%"></div>
          <div :class="['list6-class' + (statue ? ' list6move' : '')]"><img src="@/assets/list6.png" height="100%" width="100%"></div>
          <div :class="['list7-class' + (statue ? ' list7move' : '')]"><img src="@/assets/list7.png" height="100%" width="100%"></div>
          <div :class="['list8-class' + (statue ? ' list8move' : '')]"><img src="@/assets/list8.png" height="100%" width="100%"></div>
          <div class="iimg4"><img src="@/assets/img4.png" height="100%" width="100%"></div>
          <div class="iiimg4"><img src="@/assets/fensi.png" height="100%" width="100%"></div>
          <div class="text">{{ text }}</div>
         
        </div>
      </div>
    </div>
    <div class="q-class" v-show="page == 22">
      <div class="q-class" id="captureId5">
        <div class="lastpage5">
          <img src="@/assets/lastPage.png" height="100%" width="100%">
          <div :class="['list1-class' + (statue ? ' list1move' : '')]"><img src="@/assets/list1.png" height="100%" width="100%"></div>
          <div :class="['list2-class' + (statue ? ' list2move' : '')]"><img src="@/assets/list2.png" height="100%" width="100%"></div>
          <div :class="['list3-class' + (statue ? ' list3move' : '')]"><img src="@/assets/list3.png" height="100%" width="100%"></div>
          <div :class="['list4-class' + (statue ? ' list4move' : '')]"><img src="@/assets/list4.png" height="100%" width="100%"></div>
          <div :class="['list5-class' + (statue ? ' list5move' : '')]"><img src="@/assets/list5.png" height="100%" width="100%"></div>
          <div :class="['list6-class' + (statue ? ' list6move' : '')]"><img src="@/assets/list6.png" height="100%" width="100%"></div>
          <div :class="['list7-class' + (statue ? ' list7move' : '')]"><img src="@/assets/list7.png" height="100%" width="100%"></div>
          <div :class="['list8-class' + (statue ? ' list8move' : '')]"><img src="@/assets/list8.png" height="100%" width="100%"></div>
          <div class="iimg5"><img src="@/assets/img5.png" height="100%" width="100%"></div>
          <div class="iiimg5"><img src="@/assets/jiaoshi.png" height="100%" width="100%"></div>
          <div class="text">{{ text }}</div>
    
        </div>
      </div>
    </div>
    <img :src="dataURL" alt="share" v-show="page == 23" class="share-class" />
  </div>
</template>
<script>
import Vue from 'vue'
import Progress from 'vue-multiple-progress'
import 'vue-awesome-swiper/node_modules/swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import html2canvas from 'html2canvas'

Vue.use(Progress)

export default {
  name: "App",
  components: {
    swiper,
    swiperSlide
  },
  

  data: () => {
    return {
      dataURL: "",
      bgHeight: "",
      qa: false,
      qb: false,
      qc: false,
      qd: false,
      statue: false,
      count: 0,
      percent: 0,
      page: -1,
      text:"",
    };
  },
  
    
  
  mounted: function () {
    this.preload();
  },
  watch: {
    page: function (val) {
      if (val == 18 ||val == 19 ||val == 20 ||val == 21 ||val == 22 ) {
        setTimeout(() => {
          this.statue = true;
        }, 100);
      } else {
        this.statue = false;
      }
    },
    count: function (val) {
      if (val === 35) {
        setTimeout(() => {
          this.page++;
        }, 100);
      }
    },
  },
  methods: {
    start() {
      this.page++;
    },
    pushChoiceA() {
      this.qa++;
       setTimeout(() => {
          this.page++;
        }, 100);
      setTimeout(() => {
          this.qa--;
        }, 100);
    },
    pushChoiceB() {
      this.qb++;
       setTimeout(() => {
          this.page++;
        }, 100);
      setTimeout(() => {
          this.qb--;
        }, 100);
    },
    pushChoiceC() {
      this.qc++;
       setTimeout(() => {
          this.page++;
        }, 100);
      setTimeout(() => {
          this.qc--;
        }, 100);
    },
    pushChoiceD() {
      this.qd++;
       setTimeout(() => {
          this.page++;
        }, 100);
      setTimeout(() => {
          this.qd--;
        }, 100);
    },
    img(index){
      this.page = this.page + index;
      if(index == 1){
      setTimeout(() => {
        html2canvas(document.querySelector("#captureId1"), {
          scale: 3,
        }).then((canvas) => {
          console.log(canvas);
          this.dataURL = canvas.toDataURL("image/jpeg");
          this.page = 23;
        });
      }, 2500)
      }
      if(index == 2){
      setTimeout(() => {
        html2canvas(document.querySelector("#captureId2"), {
          scale: 3,
        }).then((canvas) => {
          console.log(canvas);
          this.dataURL = canvas.toDataURL("image/jpeg");
          this.page = 23;
        });
      }, 2500)
      }
      if(index == 3){
      setTimeout(() => {
        html2canvas(document.querySelector("#captureId3"), {
          scale: 3,
        }).then((canvas) => {
          console.log(canvas);
          this.dataURL = canvas.toDataURL("image/jpeg");
          this.page = 23;
        });
      }, 2500)
      }
      if(index == 4){
      setTimeout(() => {
        html2canvas(document.querySelector("#captureId4"), {
          scale: 3,
        }).then((canvas) => {
          console.log(canvas);
          this.dataURL = canvas.toDataURL("image/jpeg");
          this.page = 23;
        });
      }, 2500)
      }
      if(index == 5){
      setTimeout(() => {
        html2canvas(document.querySelector("#captureId5"), {
          scale: 3,
        }).then((canvas) => {
          console.log(canvas);
          this.dataURL = canvas.toDataURL("image/jpeg");
          this.page = 23;
        });
      }, 2500)
      }
    },
    nextPage(){
      this.page++;
    },
    preload() {
      let imgs = [
        require("./assets/logo-twt.png"),
        require("./assets/bMemory.png"),
        require("./assets/img1.png"),
        require("./assets/img2.png"),
        require("./assets/img3.png"),
        require("./assets/img4.png"),
        require("./assets/img5.png"),
        require("./assets/pageFirst.png"),
        require("./assets/pick.png"),
        require("./assets/question-one.png"),
        require("./assets/question-1.png"),
        require("./assets/question-two.png"),
        require("./assets/question-2.png"),
        require("./assets/question-three.png"),
        require("./assets/question-3.png"),
        require("./assets/question-four.png"),
        require("./assets/question-4.png"),
        require("./assets/question-five.png"),
        require("./assets/question-5.png"),
        require("./assets/question-six.png"),
        require("./assets/question-6.png"),
        require("./assets/question-seven.png"),
        require("./assets/question-7.png"),
        require("./assets/question-eight.png"),
        require("./assets/question-8.png"),        
        require("./assets/lastPage.png"),
        require("./assets/list1.png"),
        require("./assets/list2.png"),
        require("./assets/list3.png"),
        require("./assets/list4.png"),
        require("./assets/list5.png"),
        require("./assets/list6.png"),
        require("./assets/list7.png"),
        require("./assets/list8.png"),
        require("./assets/shitang.png"),
        require("./assets/xuezi.png"),
        require("./assets/fensi.png"),
        require("./assets/jiaoshi.png"),
      ];
      for (let img of imgs) {
        let image = new Image();
        image.src = img;
        image.onload = () => {
          this.count++;
          this.percent = Math.floor((this.count / 38) * 100);
          
        };
      }
    },
  },
};
    
</script>

<style>

#app {
  position: relative;
  text-align: center;
  overflow: hidden;
}
.getImg{
  font-size: 17px;
  position: absolute;
  left: 55%;
  top: 89%;
  width: 100%;
  height: 100%;
}
.share-class{
  width: 100%;
  height: 100vh;
}
.text{
  font-size: 2.2vh;
  position: absolute;
  left: 52%;
  top: 71%;
  width: 30%;
  height: 40%;
  color:maroon;
}
.textarea{
  display: flex;
      background:transparent;
      border-style:none; 
      border:0;  
    background-color:transparent;    
    height: auto;  
    outline:none; 
   resize:none; 
   overflow-y:hidden;
   overflow-x:hidden;
   font-size: 3.3vh;
  position: absolute;
  left: 28%;
  top: 80%;
  width: 70%;
  height: 40%;
  color:maroon;
  
}
.textarea::placeholder{
  
  color:rgb(197, 188, 115);
}
.iiimg5{
  position: absolute;
  left: 58%;
  top: 62%;
  width: 28%;
  height: 11%;
  
 
}
.iiimg4{
  position: absolute;
  left: 58%;
  top: 62%;
  width: 28%;
  height: 11%;
  animation: ani 1s ease;
  -webkit-animation: ani 0.4s ease;
}
.iiimg3{
  position: absolute;
  left: 58%;
  top: 62%;
  width: 28%;
  height: 11%;
  animation: ani 1s ease;
  -webkit-animation: ani 0.4s ease;
}
.iiimg2{
  position: absolute;
  left: 58%;
  top: 62%;
  width: 28%;
  height: 11%;
  animation: ani 1s ease;
  -webkit-animation: ani 0.4s ease;
}
.iiimg1{
  position: absolute;
  left: 58%;
  top: 62%;
  width: 28%;
  animation: ani 1s ease;
  -webkit-animation: ani 0.4s ease;
}
.iimg5{
  position: absolute;
  left: 11%;
  top: 60.8%;
  width: 30%;
  height: 21%;
}
.iimg4{
  position: absolute;
  left: 11%;
  top: 60.8%;
  width: 30%;
  height: 21%;
}
.iimg3{
  position: absolute;
  left: 11%;
  top: 60.8%;
  width: 30%;
  height: 21%;
}
.iimg2{
  position: absolute;
  left: 11%;
  top: 60.8%;
  width: 30%;
  height: 21%;
}
.iimg1{
  position: absolute;
  left: 11%;
  top: 60.8%;
  width: 30%;
  height: 21%;
}
.list8move {
  right: 50%;
  top: 50%;
  transform: translate(-104%,0%);
  
}
.list8-class {
  position: absolute;
  left: 100%;
  top: 53.5%;
  width: 83%;
  height: 6%;
  background-size: 100% 100%;
  transition: all 2.25s ease;
}
.list7move {
  right: 50%;
  top: 50%;
  transform: translate(-104%,0%);
  
}
.list7-class {
  position: absolute;
  left: 100%;
  top: 47.5%;
  width: 85%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 2s ease;
}
.list6move {
  right: 50%;
  top: 50%;
  transform: translate(129.3%,0%);
  
}
.list6-class {
  position: absolute;
  left: -100%;
  top: 42.2%;
  width: 80%;
  height: 6%;
 
  background-size: 100% 100%;
  transition: all 1.75s ease;
}
.list5move {
  right: 50%;
  top: 50%;
  transform: translate(-104%,0%);
  
}
.list5-class {
  position: absolute;
  left: 100%;
  top: 37%;
  width: 85%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 1.5s ease;
}
.list4move {
  right: 50%;
  top: 50%;
  transform: translate(150%,0%);
  
}
.list4-class {
  position: absolute;
  left: -100%;
  top: 31.5%;
  width: 69%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 1.25s ease;
}
.list3move {
  right: 50%;
  top: 50%;
  transform: translate(159.5%,0%);
  
}
.list3-class {
  position: absolute;
  left: -100%;
  top: 26%;
  width: 65%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 1s ease;
}
.list2move {
  right: 50%;
  top: 50%;
  transform: translate(148%,0%);
  
}
.list2-class {
  position: absolute;
  left: -100%;
  top: 20.5%;
  width: 70%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 0.75s ease;
}
.list1move {
  right: 50%;
  top: 50%;
  transform: translate(-103.8%,0%);
  
}
.list1-class {
  position: absolute;
  left: 100%;
  top: 15%;
  width: 85%;
  height: 6%;
  
  background-size: 100% 100%;
  transition: all 0.5s ease;
}
.lastpage1{
width: 100%;
  height: 100vh;
  
}
.lastpage2{
  width: 100%;
  height: 100vh;
  
}
.lastpage3{
  width: 100%;
  height: 100vh;
  
}
.lastpage4{
  width: 100%;
  height: 100vh;

}
.lastpage5{
  width: 100%;
  height: 100vh;

}
.Swiper{
  height: 46%;
  width: 60%;
  position: fixed;
  top: 22%;
  left: 21%;
  margin: 0%;
}

.wrap {
		padding: 40rpx;
	}

.loading-class {
  height: 100vh;
  width: 100%;
}
.content-class {
  width: 300px;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.cover-class {
  width: 100%;
  height: 100vh;
  background-image: url("./assets/pageFirst.png");
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
}
.start-class {
  width: 64.6vw;
  height: 35vw;
  position: absolute;
  left: 16%;
  top: 55%;
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
}

.q-class {
  width: 100%;
  height: 100vh;
  
  background-size: 100% 100%;
}

.name-class {
  text-align: center;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  width: 90px;
  color: #1b1b1c;
  font-family: Hyk1gj;
  font-size: 20px;
  position: absolute;
  top: 10%;
  left: 50%;
  transform: translateX(calc(-50% - 143px));
}

.img1{
  background-image: url("./assets/img1.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  
  
}
.img2{
  background-image: url("./assets/img2.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  
}
.img3{
  background-image: url("./assets/img3.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  
}
.img4{
  background-image: url("./assets/img4.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  
}
.img5{
  background-image: url("./assets/img5.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  
}

.q1-1-class {
  background-image: url("./assets/question-one.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q2-1-class {
  background-image: url("./assets/question-two.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q3-1-class {
  background-image: url("./assets/question-three.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q4-1-class {
  background-image: url("./assets/question-four.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q5-1-class {
  background-image: url("./assets/question-five.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q6-1-class {
  background-image: url("./assets/question-six.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q7-1-class {
  background-image: url("./assets/question-seven.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q8-1-class {
  background-image: url("./assets/question-eight.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.memory-class {
  background-image: url("./assets/bMemory.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q1-2-class {
  background-image: url("./assets/question-1.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q2-2-class {
  background-image: url("./assets/question-2.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q3-2-class {
  background-image: url("./assets/question-3.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q4-2-class {
  background-image: url("./assets/question-4.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q5-2-class {
  background-image: url("./assets/question-5.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q6-2-class {
  background-image: url("./assets/question-6.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q7-2-class {
  background-image: url("./assets/question-7.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q8-2-class {
  background-image: url("./assets/question-8.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.3;
  animation: allin 2s ease 1;
  -webkit-animation: allin 2s ease 1;
  animation-fill-mode: forwards;
}
.q-a-class {
  position: absolute;
  width: 30%;
  height: 5%;
  top: 78%;
  left: 15%;
}
.q-b-class {
  position: absolute;
  width: 30%;
  height: 5%;
  top: 78%;
  right: 20%;
}
.q-c-class {
  position: absolute;
  width: 30%;
  height: 5%;
  top: 83%;
  left: 15%;
}
.q-d-class {
  position: absolute;
  width: 30%;
  height: 5%;
  top: 83%;
  right: 20%;
}
.qa{
  background-image: url("./assets/pick.png");
  background-size: 100% 100%;
  position: absolute;
  width: 8%;
  height: 5%;
  top: 78%;
  left: 15%;
}
.qb{
  background-image: url("./assets/pick.png");
  background-size: 100% 100%;
  position: absolute;
  width: 8%;
  height: 5%;
  top: 78%;
  right: 40%;
}
.qc{
  background-image: url("./assets/pick.png");
  background-size: 100% 100%;
  position: absolute;
  width: 8%;
  height: 5%;
  top: 83%;
  left: 15%;
}
.qd{
  background-image: url("./assets/pick.png");
  background-size: 100% 100%;
  position: absolute;
  width: 8%;
  height: 5%;
  top: 83%;
  right: 40%;
}
.nextPage{
  position: absolute;
  width: 100%;
  height: 10%;
  top: 90%;
}

@keyframes allin {
  0% {
    opacity: 0.8;
  }
  100% {
    opacity: 1;
  }
}

@keyframes ani {
  0% {
    transform: scale(1.5);
  }
  10% {
    transform: scale(1.425);
  }
  25% {
      transform: scale(1.3);
    }
  50% {
    transform: scale(1.2);
  }
  75% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

@media screen and (min-width: 380px) {
  .name-class {
    transform: translateX(calc(-50% - 150px));
  }
}
@media screen and (min-width: 400px) {
  .name-class {
    transform: translateX(calc(-50% - 158px));
  }
}
@media screen and (max-width: 360px) {
  .name-class {
    transform: translateX(calc(-50% - 136px));
  }
}
@media screen and (max-width: 340px) {
  .name-class {
    font-size: 19px;
    transform: translateX(calc(-50% - 128px));
  }
}
@media screen and (max-width: 330px) {
  .name-class {
    font-size: 19px;
    transform: translateX(calc(-50% - 123px));
  }
}
@media screen and (max-width: 300px) {
  .name-class {
    transform: translateX(calc(-50% - 143px));
  }
  .q4-class,
  .cover-class,
  .q6-class,
  .rec-class {
    background-size: 375px 100%;
  }
  .results-class,
  .q2-1-class,
  .q2-2-class,
  .q3-1-class,
  .q3-2-class,
  .q5-2-class {
    width: 375px;
  }
  .start-class {
    width: 230px;
    height: 68px;
  }
}
@media screen and (min-width: 450px) {
  .name-class {
    transform: translateX(calc(-50% - 143px));
  }
  .q4-class,
  .cover-class,
  .q6-class,
  .rec-class {
    background-size: 375px 100%;
  }
  .results-class,
  .q2-1-class,
  .q2-2-class,
  .q3-1-class,
  .q3-2-class,
  .q5-2-class {
    width: 375px;
  }
  .start-class {
    width: 230px;
    height: 68px;
  }
}

</style>
