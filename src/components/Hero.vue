<template>

        <div class="row flex-lg-row-reverse align-items-center g-5 py-md-5">
            <div class="col-12 col-md-6 col-lg-6 order-2 order-md-1">
                <img src="@/assets/portrait.jpg" class="d-block mx-lg-auto img-fluid rounded shadow" alt="Bootstrap Themes" height="500" loading="lazy">
            </div>
            <div class="col-lg-6 order-1 order-md-2">
                <h1 class="display-5 fw-bold mb-3">Shaun Barratt</h1>
                    <p class="display-6 fs-2">I'm a...
                    <Transition mode="out-in">
                        <span :key="roleIndex">
                            {{ roles[roleIndex]}}!
                        </span> 
                    </Transition>
                    </p>
                <!-- <div class="d-grid gap-2 d-md-flex justify-content-md-start"> -->
                    <!-- <a  class="btn btn-primary btn-lg px-4 me-md-2" target="_blank" href="mailto:shaun@barratt.phd">Get in touch</a> -->
                    <!-- <button type="button" class="btn btn-outline-secondary btn-lg px-4">About me</button> -->
                <!-- </div> -->
            </div>
        </div>
</template>

<script>

export default {
    name: "About",
    data() {
        return {
            roleIndex: 0,
            roles: [
                "Doctoral Student",
                "Software Engineer",
                "Dad",
                "Researcher",
                "Electronics Hobbyist",
                "3D Printing Enthusiast",
                "Lecturer",
                "Gamer",
            ]
        }
    },
    mounted() {
        setInterval(() => {
            this.roleIndex = (this.roleIndex + 1) % this.roles.length;
        }, 2000);
    }
}

</script>

<style scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

</style>