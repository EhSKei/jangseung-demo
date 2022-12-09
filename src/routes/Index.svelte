<script>
    import { onMount } from "svelte";
    import Footer from "../lib/Footer.svelte";
    import Intro from "../lib/Intro.svelte";
    import Navbar from "../lib/Navbar.svelte";
    import Poster from "../lib/Poster.svelte";

    function syncVid() {
        let v = document.getElementById("posterVideo");
        v.pause();
        let c = document.getElementById("canvasContainer");
        c.addEventListener("transitionstart", () => {
            setTimeout(() => v.play(), 0);
        });
        let b = document.getElementsByClassName("introSkip")[0];
        b.addEventListener("click", () => {
            v.play();
        });
    }

    onMount(() => {
        syncVid();
        window.moveTo(0,0);
    });
</script>

<main>
    <Intro />
    <Poster />
    <Navbar />
    <section class="section">
        <div class="section-container">
            <span class="section-header">전시개요</span>
            <hr />
            <span class="section-title">장승·솟대 조사 대작전</span>
            <br />
            <p>
                나무나 돌로 다듬어 만든 사람 모양의 형상물(形象物)로 마을이나
                절의 들머리 또는 고개 등지에 세웠던 일종의 수호신이다. 마을
                사람들은 이를 신령시하여 제사를 지내거나 치성을 드리는 신앙의
                대상으로 여기기도 했다.
            </p>
            <p>
                장승의 어원은 1527년 최세진이 『훈몽자회(訓蒙字會)』(중권
                제9장)에서후(堠)를 설명하면서 ‘댱승 후’라 기록하였으며, 이
                ‘댱승’이 ‘쟝승→장승’으로 변했을 것으로 보고 있다. 장승의 한자어
                표기는 장생(長生, 長栍)으로 나타나며 조선시대에는 ‘댱생’이라
                발음했지만 이도 ‘댱승→쟝승→장승’으로 변했을 것으로 보고 있다.
            </p>
            <p>
                장승을 부르는 명칭에는 장생, 장성, 장싱, 장신, 벅수, 벅슈, 벅시,
                후, 수살, 수살막이, 수살목 등이 있다. 명칭으로 보아 장승이
                일반적인 용어이며, 한자어로는 장생(長生,
                長栍)·장성(長性)·장신(長神)·장승(張丞) 등으로도 쓰고, 사투리로
                장싱이라 부르는 곳도 있다. 벅수라는 말은 경상도 해안 지역과
                전라도에서는 장승을 벅수, 벅슈, 벅시 등으로 부른다. 이는
                법수(法首) 또는 법슈에서 온 것이 아닌가 추측되지만 확실치 않다.
                ‘법수’의 의미를 ‘신선’ 또는 ‘선인’으로 보는 이도 있다. 후(堠)는
                옛 문헌에 장승을 표현한 글자이고, 수살·수살막이·수살목 등으로
                표현한 것은 장승을 세워서 마을 안으로 들어오는 살(煞)인 나쁜
                재액을 막아 준다고 여기고 붙인 말이다.
            </p>
        </div>
    </section>
    <section class="section" style="background:lightgray">
        <div class="section-container">
            <span class="section-header">Exhibition Overview</span>
            <hr />
            <span class="section-title">장승·솟대 조사 대작전</span>
            <br />
            <p>
                Jangseung is a wooden or stone figure carved in human form and
                erected in the entrance of a village, temple or mountain pass to
                serve as guardian deity.
            </p>
            <p>
                Alternate terms include jangsaeng, beoksu and susalmok, but
                jangseung is the most common. The practice of erecting these
                guardian posts goes back to ancient times and many villages held
                rituals to worship them.
            </p>
            <p>
                While its most important function was to protect the village or
                temple against diseases, bad fortune, and tiger attacks and to
                preserve peace and prosperity in the village and the health and
                safety of travelling villagers, jangseung also served as
                guideposts that mark distances to major destinations, and in
                places that were viewed according to geomancy as lacking in
                energy, as devices of geomantic supplementation (bibo).
                Jangseung were also erected in the four corners of a village as
                gods of the four directions, and outside fortress gates as
                gatekeepers.
            </p>
        </div>
    </section>

    <Footer />
</main>
