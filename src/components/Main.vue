<template>
  <div>

    <LfTextRgImg />

    <StringOfLinks />

    <LeftTitleWithParagAndFourCols />

    <CenterTitleWithParagAndPanel />

    <SecLfTextRgImg />

    <CenterTitleWithParagAndThreeCols />

    <RegisterUser />

  </div>
</template>

<script>
import LfTextRgImg from './main-components/LfTextRgImg.vue';
import StringOfLinks from './main-components/StringOfLinks.vue';
import LeftTitleWithParagAndFourCols from './main-components/LeftTitleWithParagAndFourCols.vue';
import CenterTitleWithParagAndPanel from './main-components/CenterTitleWithParagAndPanel.vue';
import SecLfTextRgImg from './main-components/SecLfTextRgImg.vue';
import CenterTitleWithParagAndThreeCols from './main-components/CenterTitleWithParagAndThreeCols.vue';
import RegisterUser from './main-components/RegisterUser.vue';

export default {
  name: 'Main',
  components: {
    LfTextRgImg,
    StringOfLinks,
    LeftTitleWithParagAndFourCols,
    CenterTitleWithParagAndPanel,
    CenterTitleWithParagAndThreeCols,
    RegisterUser,
    SecLfTextRgImg
  }
}
</script>

<style scoped lang="scss">

</style>