<script>
    import Navbar from "../lib/Navbar.svelte";
    import Footer from "../lib/Footer.svelte";
    import { onMount } from "svelte";
    import { fade } from "svelte/transition";

    onMount(()=>{
        window.scrollTo(0,0)   })
</script>

<main transition:fade>
    <Navbar />
    <section class="hero">
        
        <div class="hero-text">
            <h1 class="hero-header">1부. 젊은 민속학자들, <br>장승과 솟대를 조사하다.</h1>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <h2 class="section-header">1-1. 장승·솟대, 조사를 계획하다.</h2>
            <hr />
            <h3 class="section-title">
                이종철(전 국립민속박물관장, 전 전통문화학교 총장)
            </h3>
            <video
            src="./chapter01/chapter01-video-02.mp4"
            controls
            class="section-video"></video>

        </div>
    </section>
    <section class="section" style="background-color: lightgray">
        <div class="section-container">
            <h2 class="section-header">1-2. 장승·솟대, 어떻게 조사하였나?</h2>
            <hr />
            <h3 class="section-title">
                이관호(국립민속박물관 민속연구과장, 당시 학예연구원)
            </h3>
            <video
                src="./chapter01/chapter01-video-02.mp4"
                controls
                class="section-video"></video>
        </div>
    </section>
    <Footer />
</main>
