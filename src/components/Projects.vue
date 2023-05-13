<template>
    <div class="container my-5 py-5">
        <div class="display-6 border-bottom pb-3">Projects</div>
        
        <!-- a card with a picture on the left -->
        
        <div class="row align-items-center my-5">
            <div class="col-md-12">
                <div v-for="project in projects" class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-25 position-relative clickable" @click="open(project)">
                    <div class="col p-4 d-flex flex-column position-static">
                        <h3 class="mb-0">{{ project.title }}</h3>
                        <div class="mb-1 text-muted">{{ project.date }}</div>
                        <p class="card-text mb-auto">
                            <div class="w-100">
                                A simple game to encourage movement using only a webcam in the web browser. Uses Psoe Estmation machine learning models from Google MoveNet
                            </div>
                        </p>
                    </div>
                    <div class="col-auto d-none d-lg-block">
                        <img src="https://via.placeholder.com/200" alt="...">
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>

export default {
    name: "Projects",
    data() {
        return {
            projects: [
                {
                    title: "SHU: Move!",
                    date: "13th May 2023",
                    description: "A simple game to encourage movement using only a webcam in the web browser. Uses Psoe Estmation machine learning models from Google MoveNet",
                    image: "https://via.placeholder.com/200",
                    link: "https://pose.serg.team/move",
                }
            ]
        }
    },
    mounted() {
        setInterval(() => {
            this.roleIndex = (this.roleIndex + 1) % this.roles.length;
        }, 2000);
    },
    methods: {
        open(project) {
            window.open(project.link, "_blank");
        }
    }
}

</script>

<style scoped>
.clickable:hover {
    cursor: pointer;
}

</style>