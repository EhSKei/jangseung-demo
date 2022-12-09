<script>
    import Navbar from "../lib/Navbar.svelte";
    import Footer from "../lib/Footer.svelte";

    import { Swiper, SwiperSlide } from "swiper/svelte";
    import { Mousewheel, Navigation, Scrollbar, EffectFade } from "swiper";

    import "swiper/css";
    import "swiper/css/mousewheel";
    import "swiper/css/navigation";
    import { fade } from "svelte/transition";
    import { onMount } from "svelte";

    let swiper;

    onMount(()=>{
        window.moveTo(0,0)
    })

    function slideToSection(n) {
        let x = document.getElementById("docSwiper");
        swiper.slideTo(n, 1000);
        window.scrollTo(0, x.offsetTop);
        
    }
</script>

<main transition:fade>
    <Navbar />
    <section class="hero" style="background-image:url('./chapter03/026.webp">
        <div class="hero-text">
            <h1 class="hero-header">3부. 장승과 솟대의 존재 양상</h1>
            <p>
                <br />
                장승․솟대는 각각 세워지기도 하지만 대개는 다른 신앙대상물과 복합적으로
                섞이면서 세워지기도 합니다.
                <br class="d-md-none" />
                <br class="d-md-none" />
                장승과 솟대는 한쌍처럼 같이 세워지는 곳이 가장 많지만 별도로 각각
                세워지는 곳도 있고, 돌탑이나 제당 등과 같이 존재하기도 합니다.
                <br class="d-md-none" />
                <br class="d-md-none" />
                국립민속박물관의 조사자료를 바탕으로 장승과 솟대의 존재 양상을 자세하게
                분류해서 살펴 보겠습니다.
            </p>
        </div>
    </section>
    <section class="section">
        <div class="section-container">
            <p class="text-center">
                장승과 솟대의 존재 형태를 분류해 보면 다음과 같습니다.<br />
            </p>
        </div>
    </section>

    <div class="chapsel-container">
        <button
            on:click="{() => slideToSection(0)}"
            class="chapsel"
            style="background-image: url(./chapter03/027.webp)"
            >장승·솟대가 각각 단독으로 존재하는 경우</button>
        <button
            on:click="{() => slideToSection(1)}"
            class="chapsel"
            style="background-image: url(./chapter03/033.webp)"
            >장승과 솟대가 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(2)}"
            class="chapsel"
            style="background-image: url(./chapter03/034.webp)"
            >장승과 탑이 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(3)}"
            class="chapsel"
            style="background-image: url(./chapter03/035.webp)"
            >장승과 선돌이 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(4)}"
            class="chapsel"
            style="background-image: url(./chapter03/036.webp)"
            >솟대와 탑이 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(5)}"
            class="chapsel"
            style="background-image: url(./chapter03/038.webp)"
            >솟대와 선돌이 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(6)}"
            class="chapsel"
            style="background-image: url(./chapter03/039.webp)"
            >장승, 솟대, 탑이 같이 있는 경우</button>
        <button
            on:click="{() => slideToSection(7)}"
            class="chapsel"
            style="background-image: url(./chapter03/040.webp)"
            >장승, 선돌, 탑이 같이 있는 경우</button>
    </div>

    <Swiper
        spaceBetween="{0}"
        slidesPerView="{1}"
        autoHeight
        initialSlide="{0}"
        noSwiping="{true}"
        on:slideChange="{() => console.log('slide change')}"
        on:swiper="{(e) => (swiper = e.detail[0])}"
        id="docSwiper"
        class="pb-5">
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h2 class="section-header">
                        1. 장승·솟대가 각각 단독으로 존재하는 경우
                    </h2>
                    <hr />
                    <h3 class="section-title pb-5">1-1. 장승만 있는 경우</h3>

                    <div class="row">
                        <img
                            src="./chapter03/027.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            (경기도 양평군 강하면 성덕2리 장승, 1988년 10월 20일
                            정종수 조사) 성덕2리 장승은 입구에 30~40년생
                            밤나무가 10여 그루 있는 길 양쪽에 위치해 있었습니다.
                            왼편에는 남자장승이, 오른편에는 여자장승이 서
                            있었습니다. 장승은 키가 거의 3미터에 이르고 얼굴 및
                            몸통에 붉은 색이 칠해져 있었습니다. 얼굴은 상하로 긴
                            형태이고 눈은 눈끝이 위로 치켜 올라간 부릅뜬
                            모양입니다. 남자장승에는 천하대장군, 여자장승에는
                            지하여장군이 적혀 있었습니다.
                        </p>
                    </div>
                    <div class="row">
                        <p class="col-lg-6 pb-5">
                            마을 길을 사이에 두고 남자장승과 여자장승이 세워져
                            있는 것은 전형적인 장승의 존재 형태입니다.
                            성덕2리에서는 마을 입구의 장승 앞에서 3년에 한번씩
                            음력 2월초 10일이나 11일에 장승제를 지내고
                            있었습니다. 마을 사람들은 제일이 정해진 날부터
                            개구리, 쥐, 벌레 등 일체의 살생을 금지한다고 하며,
                            제사가 돌아오는 해에는 김장에도 새우젓 등 비린내가
                            나는 것은 넣지 않는 풍습이 있었다고 합니다.
                        </p>
                        <img
                            src="./chapter03/027-1.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                    <img
                        src="./chapter03/027-2.webp"
                        alt=""
                        class="w-100 pb-5" />
                    <div class="row">
                        <img
                            src="./chapter03/028.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            (전라남도 순천시 낙안면 내운리 내동 벅수, 1994년 8월
                            박호원 조사) 이번에는 멀리 전라남도 순천으로
                            가보겠습니다. 벅수는 전라남도 지방에서 장승을 이르는
                            명칭입니다. 내동 벅수는 마을의 좌우에 서로 500미터
                            정도 사이를 두고 세워져 있었습니다. 마을의 왼편에는
                            여자장승인 지하여장군이, 오른편에는 남자장승인
                            천하대장군이 있었습니다. 남자장승인 천하대장군은
                            멀히에 사모를 쓰고 눈을 부릅뜬 형태입니다.
                        </p>
                    </div>
                    <div class="row">
                        <p class="col-lg-6 pb-5">
                            반면 여자장승인 지하여장군은 머리에 족두리를 쓴
                            형태로 얼굴에 지름 3cm정도의 곤지가 찍혀 있습니다.
                            여성성을 강조한 장승이었습니다. 내동에서도 장승을
                            모시는 제사를 매년 음력 정월 14일 저녁 11시에 지내고
                            있었습니다. 마을에서는 장승제를 당산제 또는 도제
                            모신다고 했다고 합니다. 제관은 3인을 선정하는데
                            특이하게도 자녀가 적은 집이 우선이라고 합니다. 그
                            이유는 자녀가 많으면 아무래도 이런저런 일들이 많이
                            일어나기 때문이였다고 합니다.
                        </p>
                        <img
                            src="./chapter03/028-1.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                    <div class="row">
                        <img
                            src="./chapter03/029.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <img src="./chapter03/030.webp" alt="" class="w-100" />
                        <p>
                            그 외에도 경상남도 창원시 북면 화천리 시화마을의
                            선돌형 장승(이관호·오세길 조사, 1996년 7월 31일)과
                            경상북도 긍릉군 아포면 송천리 숭산마을의 문인석
                            장승(정승모 조사, 1989년 2월 22일)이 있습니다. 이들
                            장승은 본래 장승으로 만들어진 것은 아니나 마을
                            사람들이 후에 장승의 기능을 부여하여 마을의
                            수호신으로 삼은 것이 특징입니다.
                        </p>
                    </div>
                </div>
            </section>
            <section class="section">
                <div class="section-container">
                    <hr />
                    <h3 class="section-title pb-5">1-2. 솟대만 있는 경우</h3>

                    <div class="row">
                        <img
                            src="./chapter03/031.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            (경기도 파주군 광탄면 용미4리 진대, 정종수 조사,
                            1988년 10월 11일) 파주군 용미4리에서는 솟대를 진대
                            혹은 짐대라 부르고 있었습니다. 마을 입구에는
                            할아버지 진대, 뒤쪽에는 할머니 진대가 있었습니다.
                            장대의 길이는 4m 정도였고 진대에 달린 새를
                            마을사람들은 기러기라 불렀습니다.
                        </p>
                    </div>
                    <div>
                        <p>
                            매년 음력 10월 초3일에 진대고사라는 마을 제사를
                            지낸다고 합니다. 진대고사가 끝나야 각 가정에서의
                            안택고사를 모실 수 있다고 합니다.
                        </p>
                        <img
                            src="./chapter03/027-1.webp"
                            alt=""
                            class="w-100 pb5" />
                    </div>
                    <div>
                        <p>
                            1988년의 진대고사에는 특별히 도당굿도 했다고 합니다.
                            당굿은 모두 12거리를 하는데, ①부정청배, ②부정거리,
                            ③불사맞이, ④장군거리, ⑤별상거리, ⑥신장거리,
                            ⑦별상대감, ⑧대감놀이, ⑨조상거리, ⑩성주거리,
                            ⑪창부거리, ⑫뒷풀이 순서로 진행하였습니다.
                        </p>

                        <Swiper
                            spaceBetween="{50}"
                            slidesPerView="{1}"
                            modules="{[Navigation]}"
                            navigation
                            loop
                            on:slideChange="{() =>
                                console.log('slide change')}">
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/031-1.webp" /></SwiperSlide>
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/031-2.webp" /></SwiperSlide>
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/31-3.webp" /></SwiperSlide>
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/31-4.webp" /></SwiperSlide>
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/31-5.webp" /></SwiperSlide>
                            <SwiperSlide
                                ><img
                                    class="w-100"
                                    src="./chapter03/31-6.webp" /></SwiperSlide>
                        </Swiper>
                    </div>
                    <div class="row">
                        <img
                            src="./chapter03/032.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            <img
                                src="./chapter03/032-1.webp"
                                alt=""
                                class="w-100 p-2" />
                            (경상북도 안동군 도산면 태자1동 고리재 오릿대, 이종철·천진기
                            조사, 1989년 2월 21일) 안동군 태자1동 고리재의 오릿대는
                            마을의 중앙에 세워져 있는 것이 특징이었습니다. 오릿대의
                            놆이는 4~5m 정도였고 길다란 소나무 장대 위에 나무로 새모양을
                            깍아서 얹어 놓은 형태입니다. 마을 사람들은 이것을 오리라
                            부르고 있었습니다. <br />
                            <img
                                src="./chapter03/032-2.webp"
                                alt=""
                                class="w-100 p-2" />
                        </p>
                    </div>
                    <img src="./chapter03/032-3.webp" alt="" class="w-100" />
                    <p>
                        마을의 입구에는 서낭당이 있어서 매년 정월대보름에 제사를
                        지낸다고 하는데 만약 오릿대가 썩어서 넘어지면 제사
                        전날에 다시 깍아서 세운다고 한다. 제사를 지낼 때도
                        오릿대 앞에서 지내는 것은 특별히 없다고 한다.
                    </p>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h2 class="section-header">
                        2. 장승과 솟대가 같이 있는 경우
                    </h2>
                    <hr />
                    <div class="row">
                        <img
                            src="./chapter03/033.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            (강원도 홍천군 동면 삼현리 장승·솟대, 박호원 조사,
                            1988년 10월 13일) 삼현리의 장승과 솟대는 마을
                            초입에서 약 500m 정도 더 들어가는 길목에 장승 4기,
                            솟대 3기가 있었습니다. 남자장승인 천하대장군은
                            사모를 쓰고 있으며, 눈·귀·입·수염은 붓으로 그렸고
                            코는 따로 나무를 깍아서 부착시켰습니다. 장승과
                            솟대가 같이 있는 전형적인 모습이었습니다.
                            <img
                                src="./chapter03/033-1.webp"
                                class="w-100"
                                alt="" />
                        </p>
                    </div>
                    <div class="row">
                        <p class="col-lg-6 pb-5">
                            삼현리에서는 2년에 한번씩 음력 정월 대보름날 달이 뜰
                            무렵에 지낸다고 합니다. 장승제를 지내는 날 아침에는
                            주민들이 모여서 야산에서 베어 온 나무로 장승과
                            솟대를 직접 제작합니다. 새로 만든 장승과 솟대는
                            기존의 것과 교체가 됩니다. 기존 장승은 근처에 그냥
                            방치한다고 합니다.
                        </p>
                        <img
                            src="./chapter03/033-2.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h2 class="section-header">
                        3. 장승과 탑이 같이 있는 경우
                    </h2>
                    <hr />
                    <p>
                        충청북도 영동군 용산면 율곡2구 섭눈이 장승과 탑, 박호원
                        조사, 1898년 11월 10일) 영동군 섭눈이 마을의 입구에서
                        우측으로 장승과 돌탑 간목(竿木)이 있고 좌측으로 너비
                        약2m 가량의 내[川]를 건너 그 바로 위쪽에 장승, 돌탑,
                        신목이 있었습니다. 섭눈이 마을의 장승은 몸체에 명문이
                        조각되거나 묵서되어 있지 않다는 점과 우측 장승 뒤의
                        간목도 ‘장승’이라고 하는 점입니다. 돌탑의 상부에는
                        머리와 몸통을 지닌 마치 거북 모양과 같은 돌이 하나
                        올려져 있고 목부분에 금줄이 걸처져 있는게
                        특징이었습니다.
                    </p>
                    <Swiper
                        spaceBetween="{50}"
                        slidesPerView="{1}"
                        modules="{[Navigation]}"
                        navigation
                        autoHeight
                        loop
                        on:slideChange="{() => console.log('slide change')}">
                        <SwiperSlide
                            ><img
                                class="w-100"
                                src="./chapter03/034.webp" /></SwiperSlide>
                        <SwiperSlide
                            ><img
                                class="w-100"
                                src="./chapter03/034-1.webp" /></SwiperSlide>
                        <SwiperSlide
                            ><img
                                class="w-100"
                                src="./chapter03/034-2.webp" /></SwiperSlide>
                        <SwiperSlide
                            ><img
                                class="w-100"
                                src="./chapter03/034-3.webp" /></SwiperSlide>
                    </Swiper>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h1 class="section-header">
                        4. 장승과 선돌이 같이 있는 경우
                    </h1>
                    <hr />
                    <img src="./chapter03/035.webp" alt="" class="w-100" />
                    <p>
                        (울산광역시 울주구 언양읍 남부2리 장승과 선돌,
                        박호원·기량 조사, 1996년 3월 3일) 본래 언양 장승은
                        울산에서 언양으로 들어오는 입구에 해당하는 옛길 양편에
                        있었으며 이곳 주민들은 이곳을 ‘벅시골’이라고 부릅니다.
                        장승 옆에는 자연석의 입석 1기가 세워져 있는데, 주민들은
                        이를 미륵보살 또는 미륵불이라고 부릅니다. 1957년에는
                        이곳에 신당(神堂)을 만들고 당 내부에 장승을 봉안하려
                        하였으나 1993년 35번 국도의 확장으로 모두 철거되었다고
                        합니다. 신당이 철거되던 날에는 무당을 불러 굿을 하였고
                        현재의 위치에 장승을 다시 세웠다고 합니다.
                    </p>
                    <div class="row">
                        <img
                            src="./chapter03/035-1.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <img
                            src="./chapter03/035-2.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                    <div class="row">
                        <img
                            src="./chapter03/035-3.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            벅시골에서는 2년에 한번씩 음력 2월 초하룻날에
                            장승제를 지냅니다. 이를 마을사람들은 동제 혹은
                            당제라 부릅니다. 마을에서는 장승을 장성이라고
                            보르기도 합니다. 벅시골이란 지명으로 보아 마을에서는
                            장승을 벅수 혹은 벅시라고도 불렀을 것입니다.
                        </p>
                    </div>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h1 class="section-header">
                        5. 솟대와 탑이 같이 있는 경우
                    </h1>
                    <hr />
                    <div class="row">
                        <img
                            src="./chapter03/036.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <p class="col-lg-6 pb-5">
                            (전라남도 곡성군 삼기면 노동리 남계마을 짐대와 탑,
                            김종대·박호원 조사, 1994년 11월) 곡성군 남계마을
                            사람들의 수호신은 마을 입구에 있는 탑과
                            짐대(솟대)였습니다. 탑과 짐대는 특이하게도
                            당산나무와 같이 있는 것이 특징입니다. 탑은 흡사
                            축대와 비슷한 형태로 돌을 쌓아서 만들었고, 탑 주위에
                            높이 4m가량의 짐대 3기가 세워져 있습니다.
                            마을사람들은 짐대의 새모양을 오리라 부릅니다.
                        </p>
                    </div>
                    <div class="row">
                        <p class="col-lg-6 pb-5">
                            (전라북도 순창군 구림면 금창리 2구 금상마을 짐대와
                            탑, 박호원·이관호 조사, 1993년 7월) 순창군
                            금상마을은 3면이 산으로 둘러싸여 있는 전형적인
                            산촌마을입니다. 마을 양옆으로는 조그마한 냇가가 있어
                            예로부터 금상마을을 풍수상 배의 형국을 한 지세라고
                            합니다. 따라서 마을 내에서 우물을 파면 물속으로
                            가라앉는다는 믿음이 있어 절대로 마을에서는 샘을 파지
                            않은 대신 마을 뒷산 골짜기에서 물을 길어 식수로
                            사용하고 있었습니다. 마을 입구에는 짐대와 돌탑을
                            세워 마을의 안전을 기원하고 있었습니다. 원래
                            금상마을에는 마을 입구 양쪽으로 할아버지탑과
                            할머니탑 등 두 개의 돌탑이 짐대(솟대)와 같이
                            있었다고 하는데, 할머니탑은 오래 전에 없어졌다고
                            합니다.
                        </p>
                        <img
                            src="./chapter03/037.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h1 class="section-header">
                        6. 솟대와 선돌이 같이 있는 경우
                    </h1>
                    <hr />
                    <div class="row">
                        <img
                            src="./chapter03/038.webp"
                            alt=""
                            class="w-100 pb-5" />
                    </div>
                    <div class="row">
                        <p class="col-lg-6 pb-5">
                            (전라북도 부안군 보안면 우동리 짐대와 선돌, 정승모
                            조사, 1991년 3월) 부안군 우동리는 부안 김씨들이 많이
                            사는 지역으로 조선 숙종때 실학자 반계 유형원이
                            살았던 곳이다. 마을사람들은 반계 유형원 선생이
                            병란을 피해 이곳에 왔을 때 우동리의 짐대와 선돌을
                            세웠다고 믿고 있습니다. 짐대는 격년으로 정월
                            대보름날 세우는데, 짐대에 60m되는 암줄과 수줄을 메고
                            농악을 치며 마을 한 바퀴 돈 후 남녀로 나누어
                            줄다리기를 합니다. 이때 여자 쪽이 이겨야 풍년이
                            든다는 믿음이 있습니다. 줄다리기가 끝나면 동아줄은
                            솟대 밑에 감아 둡니다.
                        </p>
                        <img
                            src="./chapter03/038-1.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h1 class="section-header">
                        7. 장승, 솟대, 탑이 같이 있는 경우
                    </h1>
                    <hr />
                    <img src="./chapter03/039.webp" alt="" class="w-100 pb-5" />
                    <p>
                        (충청북도 옥천군 군서면 사정리 사기점골 장승·솟대·탑,
                        이종철·정종수 조사, 1989년 2월 22일) 옥천군 사기점골은
                        고려시대부터 청자와 백자를 굽던 곳이어서 지명을
                        사기(沙器)라 하였다고 합니다. 지금도 마을의 뒷산의
                        중턱에 오르면 사기편이 많이 발견된다고 합니다. 사기점골
                        입구 오른편에는 시멘트로 약 70cm 정도 높이로 쌓은 단
                        위에 장승, 솟대, 돌탑이 세워져 있습니다. 솟대의 새는
                        떨어져 나가서 없어졌고 장대만 남아 있었습니다. 마을
                        사람들은 새를 물오리라 불렀습니다. 장승은 밤나무로 깍은
                        것으로 2기가 세워져 있습니다. 돌탑은 냇가에서 나온 돌로
                        윗부분이 다소 뾰족하게 쌓아 올려 있습니다.
                    </p>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
                <button
                    class="section-next"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex + 1);
                    }}">
                    다음
                </button>
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <section class="section">
                <div class="section-container">
                    <h1 class="section-header">
                        8. 장승, 선돌, 탑이 같이 있는 경우
                    </h1>
                    <hr />
                    <img src="./chapter03/040.webp" alt="" class="w-100 pb-5" />
                    <p>
                        (충청북도 괴산군 청천면 고성리 승암마을 장승·선돌·돌탑,
                        박호원 조사, 1989년 2월 23일) 괴산군 승암마을은 버스조차
                        다니지 않는 산골 오지 마을이었습니다. 농지 면적도 좁아서
                        겨우 마을에서 먹을 정도만 생산되었다고 합니다.
                        지리적으로 외부와 단절되어 있어서 오히려 마을
                        사람들끼리의 결속력은 높았다고 합니다. 마을에서는 장승을
                        ‘장군’이라 불렀습니다. 낙영산의 한줄기인 진산중턱에
                        ‘산제당’이 있고 마을 입구에는 장승․선돌․돌탑․신목이 놓여
                        있었습니다.
                    </p>
                    <div class="row">
                        <img
                            src="./chapter03/040-1.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                        <img
                            src="./chapter03/040-2.webp"
                            alt=""
                            class="col-lg-6 pb-5" />
                    </div>
                </div>
            </section>
            <div class="section-controls">
                <button
                    class="section-prev"
                    on:click="{() => {
                        window.scrollTo(
                            0,
                            document.getElementById('docSwiper').offsetTop
                        );
                        swiper.slideTo(swiper.activeIndex - 1);
                    }}">
                    이전
                </button>
                <button
                    class="section-top"
                    on:click="{() =>
                        window.scrollTo(
                            0,
                            document.querySelector('.chapsel').offsetTop
                        )}">
                    위로 가기
                </button>
            </div>
        </SwiperSlide>
    </Swiper>

    <Footer />
</main>
