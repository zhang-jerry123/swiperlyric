<template>
    <div class="player">
        <div class="middleL" @click="changeMiddle">
            <transition name="middlecd">
                <div class="middle-cd" v-show="currentshow==='cd'">
                    <div class="cd-wrap">
                        <!-- <div class="cd" :class="cdCls"> -->
                            <img :src='currentSong[0].image' class="image">
                        <!-- </div> -->
                    </div>
                </div>
            </transition>
            <transition name="middleLaric">
                <div class="middle-lyric" v-show="currentshow==='lyric'">
                    
                </div>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            currentshow:'cd',
            currentSong:[
                {'image':'https://i1.kknews.cc/SIG=2ru26a9/ctp-vzntr/15301131549198023s8q5n0.jpg',
                'lyric':['abc','rgk',"me and you"],
                'duration':['3','3','5']}
            ]
            
        }
    },
    methods:{
        changeMiddle(){
            if(this.currentshow==='cd'){
                this.currentshow='lyric',
                console.log(this.currentSong[0].image)
                
            }else{
                this.currentshow='cd',
                console.log(this.currentSong[0].image)
            }
        }
    }
}
</script>

<style lang="scss" scoped>
.player{
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: 150;
    .middleL {
      display: flex;
      align-items: center;
      position: fixed;
      width: 100%;
      top: 80px;
      bottom: 170px;
      font-size: 0;
      .middle-cd{
        display: inline-block;
        vertical-align: top;
        position: relative;
        width: 100%;
        height: 0;
        padding-top: 80%;
        .image{
          position: absolute;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
          border-radius: 50%;
      }
      }
    }
}
</style>>
