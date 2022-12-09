<script>
    import Chapter02Menu from "../lib/Chapter02Menu.svelte";
    import Footer from "../lib/Footer.svelte";
    import AOS from "aos";
    import "aos/dist/aos.css";
    import { onMount } from "svelte";
    import Navbar from "../lib/Navbar.svelte";
    import { fade } from "svelte/transition";

    onMount(() => {
        window.moveTo(0,0);
        let x = document.getElementsByTagName("section");
        for (let i = 0; i < x.length; i++) {
            x[i].setAttribute("data-aos", "fade-up");
        }

        AOS.init({
            offset: 500,
        });
    });
</script>

<main transition:fade>
    <Navbar />
    <section class="hero" style="background-image:url('./chapter02/023.webp">
        <div class="hero-text">
            <h1 class="hero-header">2-3. 장승과 솟대의 만남</h1>
            <p>
                형태상 장간(長竿)에 새가 올려져 있는 실물로 연대가 가장 올라가는
                것은 1749년에 건립된 부안군 계화면 대벌리의 석조간(石鳥竿)이
                있습니다. 솟대의 지역분포를 살펴보면 중부지방에서 남부지방으로
                내려갈수록 더 집중적으로 나타나고 있습니다. 솟대의 종류는 마을의
                액막이와 풍농을 위하여 세우는 일반솟대, 행주형 지세를 돛대로서
                세우는 솟대, 급제를 기념하는 솟대로 나눌 수 있습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <div class="row">
                <img src="./chapter02/024.webp" alt="" class="col-lg-6 pb-5" />
                <p class="col-lg-6 pb-5">
                    솟대가 마을입구에 건립되어 수호신으로 신앙된 시기는 빨라야
                    조선 후기를 앞서지는 못할 것으로 보입니다. 수호신으로서
                    신앙되기 전에 먼저 풍수상 목적으로 석간의 건립이 성행되었고,
                    경제적으로 다소 열세인 일반 서민들은 솟대로써 이에 충당한
                    것이 아닌가 추측됩니다.
                </p>
            </div>
            <div class="row">
                <p class="col-lg-6 pb-5">
                    오늘날 솟대 자체는 독립적인 신앙대상물로서의 성격은 매우
                    희미해졌고, 대개는 장승 또는 기타의 신앙대상물과 함께
                    모셔집니다. 그 가운데 장승과 솟대가 하나의 짝이 되는 경우가
                    가장 많습니다. 장승과 솟대가 하는 일을 나누어서 생각하고
                    모시는 마을은 거의 찾아보기 어렵습니다. 솟대의 원래 의미도
                    많이 상실되면서 장승과 결부되어 보호신 같은 역할을 하게
                    되었던 것 같습니다.
                </p>
                <img src="./chapter02/025.webp" alt="" class="col-lg-6 pb-5" />
            </div>
        </div>
    </section>

    <Chapter02Menu />
    <Footer />
</main>
