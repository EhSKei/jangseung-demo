<script>
    import Navbar from "../lib/Navbar.svelte";
    import Footer from "../lib/Footer.svelte";
    import Chapter02Menu from "../lib/Chapter02Menu.svelte";
    import { onMount } from "svelte";

    onMount(()=>{
        window.moveTo(0,0)    })
</script>

<main>
    <Navbar />
    <section class="hero">
        <div class="hero-text">
            <h1 class="hero-header">2부. 한국 장승·솟대의 역사</h1>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <img src="./chapter02/001.webp" alt="" class="section-image" />
            <p>
                마을은 가장 기본적인 사회 구성체입니다. 전통사회 마을에서는 마을
                공동의 번영과 안녕을 기원하는 여러 가지 마을공동체 신앙이
                있었습니다. 마을 구성원들은 마을의 안녕을 상징하는 대상물인
                서낭당·국사당·당산·장승·솟대·탑·선돌·당수나무 등에 신앙행위를
                하였습니다. 그 가운데 가장 잘 알려진 대표적인 유형은
                성황당(서낭당)입니다. 성황당은 여러 가지 형태로 존재합니다.
                나무만 있기도 하며, 돌탑이 있는 경우도 있으며, 우리가 주목하는
                장승과 솟대가 있는 경우도 있습니다. 장승과 솟대는 성황당과는
                별개로 마을 입구의 상징물로서의 역할을 하기도 합니다.
            </p>
        </div>
        <div class="section-container">
            <img src="./chapter02/002.webp" alt="" class="section-image" />
            <p>
                장승과 솟대가 언제부터 이 땅에 생기기 시작되었는지는 확실하지
                않습니다만, 국립중앙박물관 소장의 농경문 청동기의 앞면에는
                솟대처럼 보이는 새가 새겨져 있습니다. 이것으로 보아 솟대는
                상당히 오래 전부터 있었던 것으로 추정해 볼 수 있습니다.
            </p>
        </div>
    </section>
    <Chapter02Menu/>
    <Footer />
</main>
