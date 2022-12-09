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
    <section class="hero" style="background-image:url('./chapter02/013.webp">
        <div class="hero-text">
            <h1 class="hero-header">2-2. 솟대의 역사</h1>
            <p>
                흔히 장승과 함께 마을입구에 세워지는 대표적인 장승 복합신앙물로
                솟대를 들 수 있습니다. 솟대란 나무나 돌로 만든 새를 장대나
                돌기둥 위에 앉힌 마을의 신앙대상물입니다. 솟대는 농경마을을
                사회구성의 기초단위로 했던 때부터 마을의 안녕과 수호를 맡고
                농사의 성공을 보장하는 마을 신의 하나로 성격을 굳혀 갔습니다.
                그리고 이 솟대는 풍수지리 사상과 과거급제에 의한 입신양명의
                풍조가 널리 퍼짐에 따라 행주형 지세에 돛대로서 세우는 짐대와
                급제를 기념하기 위한 화주대로 분화 발전되었습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <img src="./chapter02/014.webp" alt="" class="w-100 pb-5" />
            <p>
                솟대의 역사는 앞에서 언급한 '농경문 청동기'의 솟대를 근거로
                청동기시대까지 보는 것이 통설입니다. 그러나 이후 솟대는 조선
                후기까지 유물로나 문헌상으로도 전혀 그 내력을 남기고 있지 않아
                솟대의 역사적 전승력에서 상당한 공백기가 있습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <h2 class="section-header">(1) 솟대의 시원</h2>
            <hr />
            <div class="row">
                <img src="./chapter02/015.webp" alt="" class="col-lg-6 pb-5" />
                <p class="col-lg-6 pb-5">
                    솟대에 대한 신앙은 북아시아 여러 민족에게 공통되게 나타나는
                    현상입니다. 또한 이 지역 청동기시대의 의기(儀器)에도
                    나뭇가지 기둥에 새를 앉힌 조형물이나 문양이 간혹 발견됩니다.
                    이처럼 넓은 지역성과 오랜 시간성은 솟대가 고대로부터
                    북아시아 전 지역에 퍼져나간 보편적인 신앙요소임을
                    알려줍니다.
                </p>
            </div>
            <div class="row">
                <p class="col-lg-6 pb-5">
                    긴 장대 위에 새를 부착시킨 형태의 조간(鳥竿)은 동부
                    시베리아의 오로치(Orochee), 오스챠(Ostachak)족,
                    골대(Goldi)족, 만주 몽고족 그리고 북미 인디안(Tungus)족의
                    분포지와 함께 고려해 볼 수 있는 단서를 제공해줍니다. 다시
                    말해 솟대의 형태와 유사한 조간은 이들 퉁구스족의 독특한
                    신앙물로 여겨지는 것입니다.
                </p>
                <img src="./chapter02/016.webp" alt="" class="col-lg-6 pb-5" />
            </div>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <h2 class="section-header">(2) 소도와 솟대</h2>
            <hr />
            <img src="./chapter02/017.webp" alt="" class="w-100 pb-5" />
            <p>
                문헌기록 상으로 중국 측 문헌인『삼국지』,「위지」, 동이전,
                한조(韓條) 등에 삼한지역의 소도에 관한 언급이 보이는데, 소도와
                솟대의 발음상 유사성을 근거로 삼한시대 솟대 존재론이 주장되고
                있습니다. 하지만 소도와 솟대의 종교적, 발음상 유사성만을 근거로
                솟대와 소도의 연관성을 주장하는데는 한계가 있습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <h2 class="section-header">
                (3) 불교전래에 따른 입목습속(立木習俗)과 당간(幢竿)
            </h2>
            <hr />
            <div class="row">
                <img src="./chapter02/018.webp" alt="" class="col-lg-6 pb-5" />
                <p class="col-lg-6 pb-5">
                    고대신앙과 종교의 요소들은 삼국시대 불교유입으로 많은 변화를
                    겪습니다. 토착신앙과 불교와의 만남은 삼국시대 이후
                    통일신라에 걸치는 문화복합이 이루어졌습니다. 불교사찰에서
                    흔히 볼수 있는 당간을 불교 수입 이전의
                    입목습속(立木習俗)과의 관련에 주목해야 합니다. 당간의 관념과
                    형태가 솟대와 유사하고 제천신간(祭天神竿)이 당간이라는
                    형태로 수용되었다는 주장이 있습니다. 불교는 다른 종교보다
                    포용성이 크기 때문에 그것을 받아들인 민족에 따라 개성 있는
                    불교가 형성되었고, 고대 한국인에게 천신은 불교수용 후에도 그
                    존엄을 잃지 않았습니다. 재래의 천신신앙은 어떠한 형태로든
                    불교에 수용되지 않으면 안 되는데, 당간은 천신이 조형으로
                    온존하게 된 것이라고 하겠습니다.
                </p>
            </div>
            <div class="row">
                <p class="col-lg-6 pb-5">
                    신라·고려시대 절터의 당간지주는 유물로서 많이 남아 있습니다.
                    그러나 현재 사용되고 있지 않아서 용도가 무엇인지 본래의
                    형태는 어떤 것인지 막연합니다. 다만 그 명칭에서 깃발을 다는
                    대(竿)라고 짐작을 하고 있지만 인도나 중국의 당과 그 형태가
                    다름으로써, 불교 조형을 통한 한국불교의 특수성을 논할 때
                    누구나 당간에 주목하게 됩니다. 당간은 사찰의 표시라고 할 수
                    있지만 그것 자체가 예배당인 제천간(祭天竿)입니다. 그
                    형태에서도 주변 불교국의 당간과 비교할 수 없는 독특한
                    것입니다.
                </p>
                <img src="./chapter02/019.webp" alt="" class="col-lg-6 pb-5" />
            </div>
            <img src="./chapter02/020.webp" alt="" class="w-100 pb-5" />
            <p>
                짐대는 불교사찰의 당간과 민속 상의 솟대를 모두 지칭하는 말로도
                사용됩니다. 솟대는 우선 '솟대', '솔대'라는 명칭과 같이 '솟아
                있는 장대'가 필수 요건이 됩니다. 솟대의 한 명칭인 짐대와 진대는
                불교사찰의 당간을 지칭하는 동시에 선박의 돛대를 뜻하기 때문에
                행주형 지세에 마을에 세우는 돛대도 일반적으로 짐대라고 부릅니다.
                그러나 행주형 지세와 관련이 없는 솟대도 흔히 짐대라고 부릅니다.
                짐대란 대개 길게 뻗어 있는 사물을 가리키기 때문입니다.
            </p>
            <img src="./chapter02/021.webp" alt="" class="w-100 pb-5" />
            <p>
                충남 공주군 반포면 상신리 마을에는 고려시대에 건립된 것으로
                추정되는 구룡사(九龍寺) 당간지주가 아직 남아 있는데, 마을
                사라들은 이것을 짐대라고 부릅니다. 충남 홍성군 홍성읍에서도
                그곳의 당간지주를 짐대라고 부릅니다. 이러한 현상은 민속 상의
                솟대와 불교사찰의 당간과의 관계성을 잘 보여주는 것이라고
                생각됩니다. 이처럼 당간의 특성과 솟대와 당간을 함께 지칭하여
                '짐대'라는 명칭을 고려할 때 입간으로서 솟대의 역사성이 인정될 수
                있습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <h2 class="section-header">(4) 고려의 장간(長竿) 풍속</h2>
            <hr />
            <img src="./chapter02/022.webp" alt="" class="w-100 pb-5" />
            <p>
                『고려도경』에 압승물로서 긴 장대를 세우는 풍속을 기록하고 있어
                장간풍속으로서의 솟대의 역사적 공백기가 어느 정도 재구성될
                가능성도 있습니다. "옛날에 전하기를 창우(倡優)들이 거주하는데 긴
                장대를 걸어서 일반인 집과 구별하였다. 지금 그렇지 않다고
                들었는데 이 풍속은 음사(淫祠) 귀신(鬼神)을 쫓고 압승(壓勝)을
                비는 도구이다"라 하여 고려시대에 장간이 벽사의 도구로 신앙시된
                사례를 볼 수 있습니다.
            </p>
        </div>
    </section>

    <Chapter02Menu />
    <Footer />
</main>
