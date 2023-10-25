<template>
    <section class="job-opport-sec">
        <h2 class="job-opport-sec__main-title"><span class="italic">Latest</span> 10 job oportunities</h2>
        <div>
            <p class="job-opport-sec__city-name">City:</p>
        </div>
        <JobCard />
        <JobCard />
        <div class="job-opport-sec__button-section">
            <div class="job-opport-sec__button-wrapper">
                <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 60 60" fill="none">
                    <g opacity="0.25">
                    <circle cx="30" cy="30" r="29" transform="rotate(-180 30 30)" stroke="#014750" stroke-width="2"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M28.5726 35.7614L23.3874 30.5761C23.0692 30.2579 23.0692 29.7421 23.3874 29.4239L28.5726 24.2386C28.8908 23.9205 29.4067 23.9205 29.7249 24.2386C30.0431 24.5568 30.0431 25.0727 29.7249 25.3909L27.6377 27.4781C27.0077 28.1081 27.4539 29.1852 28.3448 29.1852L36.1852 29.1852C36.6352 29.1852 37 29.55 37 30C37 30.45 36.6352 30.8148 36.1852 30.8148L28.3448 30.8148C27.4539 30.8148 27.0077 31.8919 27.6377 32.5219L29.7249 34.6091C30.0431 34.9273 30.0431 35.4432 29.7249 35.7614C29.4067 36.0795 28.8908 36.0795 28.5726 35.7614Z" fill="#014750"/>
                    </g>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 60 60" fill="none">
                    <circle cx="30" cy="30" r="29" stroke="#0AD582" stroke-width="2"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M31.4274 24.2386L36.6126 29.4239C36.9308 29.7421 36.9308 30.2579 36.6126 30.5761L31.4274 35.7614C31.1092 36.0795 30.5933 36.0795 30.2751 35.7614C29.9569 35.4432 29.9569 34.9273 30.2751 34.6091L32.3623 32.5219C32.9923 31.8919 32.5461 30.8148 31.6552 30.8148H23.8148C23.3648 30.8148 23 30.45 23 30C23 29.55 23.3648 29.1852 23.8148 29.1852H31.6552C32.5461 29.1852 32.9923 28.1081 32.3623 27.4781L30.2751 25.3909C29.9569 25.0727 29.9569 24.5568 30.2751 24.2386C30.5933 23.9205 31.1092 23.9205 31.4274 24.2386Z" fill="#0AD582"/>
                </svg>
            </div>
            <a href="#" class="job-opport-sec__button-section-text">See all job oportunities</a>
        </div>
    </section>
</template>

<script setup>
import JobCard from '../Elements/JobCard.vue';
</script>

<style lang="scss" scoped>
@import '../../assets/main.scss';
.job-opport-sec{
    padding: 60px 0 50px 15px;
    
}
.job-opport-sec__main-title{
    font-family: $font;
    font-weight: 500;
    font-style: normal;
    line-height: 1.1;
    max-width: 600px;
    margin-bottom: auto;
    user-select: none;
    color: $dark-green;
    margin-bottom: 22px;
}

.job-opport-sec__city-name{
    font-family: $font;
    font-size: 12px;
    font-weight: 500;
    font-style: normal;
    line-height: 1.1;
    color: $dark-green;
    margin-bottom: 30px;
}


.job-opport-sec__button-section{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 15px;
}

.job-opport-sec__button-wrapper{
    display: flex;
    gap: 10px;
    margin-right: auto;

}

.job-opport-sec__button-section-text{
    font-family: $font;
    font-size: 16px;
    font-weight: 600;
    font-style: normal;
    line-height: 1.1;
    color: $dark-green;
}

</style>