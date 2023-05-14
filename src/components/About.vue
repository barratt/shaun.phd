<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col-12 col-md-7">
                <div class="display-6 border-bottom mb-3 pb-2">About me</div>
                <div class="text-secondary">
                    I'm a Ph.D student at <a href="https://www.shu.ac.uk/" target="shu">Sheffield Hallam University</a> with the <a href="https://serg.team" target="serg">Sports Engineering Research Group</a>, researching the use of machine learning to improve the
                    performance of elite level athletes. I'm also a master of software engineering, working on a variety of projects. I've been a full stack developer for over 10 years, and have worked on and led teams in a variety of projects, from small websites to large scale
                    e-commerce platforms and referencing software serving over 500k requests per day
                </div>
            </div>
            <div class="col mt-3 mt-md-0">
                <div class="display-6 border-bottom mb-3 pb-2">Contact</div>

                <div class="fs-4 clickable" @click="open('mailto:shaun@barratt.phd')"><i class="bi-envelope me-2"></i> shaun@barratt.phd</div>
                <div class="fs-4 clickable" @click="open('https://www.linkedin.com/in/shaun-barratt/')"><i class="bi-linkedin me-2"></i> shaun-barratt</div>
                <div class="fs-4 clickable" @click="open('https://github.com/barratt')"><i class="bi-github me-2"></i> barratt</div>
                <div class="fs-4 clickable" @click="open('https://barratt.phd')"><i class="bi-globe me-2"></i> barratt.phd</div>
                <div class="fs-4 clickable" @click="open('https://www.google.com/maps/place/Sheffield/@53.3957905,-1.5820274')"><i class="bi-geo-alt me-2"></i> Sheffield, UK</div>

            </div>
        </div>
    </div>
</template>

<style scoped>
.clickable {
    cursor: pointer;
}

</style>

<script>

export default {
    methods: {
        open(url) {
            window.open(url, "_blank");
        }
    }
}

</script>