<template>
  <div class="row g-0">
    <div id="testimonialSection">
      <div
        class="testimonialComponent animated fadeIn"
        v-for="CompanyStatisticData in CompanyStatisticsData"
        :key="CompanyStatisticData.statisticValue"
      >
        <div class="testimonialIcon">
          <i :class="CompanyStatisticData.statisticIcon" aria-hidden="true"></i>
        </div>
        <div class="boldTxt testimonialTxt">
          {{ CompanyStatisticData.statisticValue }} <br />{{
            CompanyStatisticData.statisticName
          }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { CompanyStatisticsData } from "../Data/statisticsData";

export default {
  data() {
    return {
      CompanyStatisticsData
    };
  }
};
</script>
