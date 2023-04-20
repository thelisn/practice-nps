<template>
  <div>
    
    <!-- 여기다가 컴포넌트들 다 모은 후 이 파일을
    App.vue에다가 넣기 -->

    <MyHeader />
    <TopScroll />
    <MainBanner />
    <OftenService />
    <PersonalService />
    <NewNews />
    <PopUp />
    <SocialNetwork />
    <IntroStat />
    <EasyKnow />
    <PuzzleBox />
    <BotFirst />
    <BotSecond />
    <BotThird />
    <br>
    <br>
    <!-- <MyHistory /> -->
    
  </div>
</template>

<script>
import MyHeader from './MyHeader.vue';
import TopScroll from './elements/TopScroll.vue';
import MainBanner from './elements/MainBanner.vue';
import OftenService from './elements/OftenService.vue';
import PersonalService from './elements/PersonalService.vue';
import NewNews from './elements/NewNews.vue';
import PopUp from './elements/PopUp.vue';
import SocialNetwork from './elements/SocialNetwork.vue';
import IntroStat from './elements/IntroStat.vue';
import EasyKnow from './elements/EasyKnow.vue';
import PuzzleBox from './elements/PuzzleBox.vue';
import BotFirst from './elements/BotFirst.vue';
import BotSecond from './elements/BotSecond.vue';
import BotThird from './elements/BotThird.vue';
// import MyHistory from './MyHistory.vue';

export default {
  components: {
    MyHeader,
    TopScroll,
    MainBanner,
    OftenService,
    PersonalService,
    NewNews,
    PopUp,
    SocialNetwork,
    IntroStat,
    EasyKnow,
    PuzzleBox,
    BotFirst,
    BotSecond,
    BotThird,
    // MyHistory
  }
}

</script>

<style scoped lang="scss">
</style>