<script>
    import { link } from "svelte-spa-router";

    import { Swiper, SwiperSlide } from "swiper/svelte";
    import { Mousewheel, FreeMode } from "swiper";

    import "swiper/css";
    import "swiper/css/mousewheel";
    import { onMount } from "svelte";

    const navItems = [
        {
            title: "HOME",
            subtitle: "",
            link: "/",
        },
        {
            title: "들어가는 글",
            subtitle: "왜 장승 솟대인가?",
            link: "/prologue",
        },
        {
            title: "1부",
            subtitle: "젊은 민속학자들, 장승과 솟대를 조사하다.",
            link: "/chapter01",
        },
        {
            title: "2부",
            subtitle: "한국 장승·솟대의 역사",
            link: "/chapter02",
            subitems: [
                {
                    title: "장승의 역사",
                    subtitle: "",
                    link: "/chapter02-1",
                },
                {
                    title: "솟대의 역사",
                    subtitle: "",
                    link: "/chapter02-1",
                },
                {
                    title: "장승과 솟대의 만남",
                    subtitle: "",
                    link: "/chapter02-1",
                },
            ],
        },
        {
            title: "3부",
            subtitle: "장승과 솟대의 존재 양상",
            link: "/chapter03",
        },
        {
            title: "4부",
            subtitle: "전국의 장승·솟대를 조사하라!",
            link: "/chapter04",
            subitems: [
                {
                    title: "1988년, 서울 올림픽의 해",
                    subtitle: "경기도, 강원도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "1989년, 장승·솟대 조사의 성숙기",
                    subtitle: "경상북도, 충청북도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "1990년, 장승·솟대 조사의 성장기",
                    subtitle: "충청남도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "1991~1995년, 장승·솟대 조사의 비약적 성장기",
                    subtitle: " 전라북도, 전라남도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "1996~1997년, 장승·솟대 조사 피날레",
                    subtitle: "경상남도(제주도) 조사",
                    link: "/chapter04-1",
                },
            ],
        },
        {
            title: "끝내는 글",
            subtitle: "10년 동안의 기나긴 여정, 전국 장승·솟대조사 대작전",
            link: "/epilogue",
        },
    ];

    let activated = false;

    function resizeCanvas() {
        let c = document.getElementsByClassName("nav")[0];
        // @ts-ignore
        c.style.height = window.innerHeight + "px"
        // @ts-ignore
        console.log(c.style.width)
    }

    onMount(() =>{
        resizeCanvas();
        window.addEventListener("resize",resizeCanvas)
    })
</script>

<button
    class="nav-open"
    on:click="{() => {
        activated = true;
        console.log(activated);
    }}">
    <img src="./navbar/menu.svg" alt="" class="nav-open-image" width="30" />
</button>

<nav class="nav" class:activated>
    <div class="nav-container">
        <div class="nav-top">
            <button
                class="nav-close"
                on:click="{() => {
                    activated = false;
                    console.log(activated);
                }}">
                <img
                    src="./navbar/close.svg"
                    alt=""
                    class="nav-close-image"
                    width="30" />
            </button>
        </div>

        <div class="nav-bottom">
            <Swiper
                slidesPerView="{'auto'}"
                direction="{'vertical'}"
                centeredSlides="{true}"
                modules="{[Mousewheel, FreeMode]}"
                mousewheel
                
                speed="{100}"
                on:slideChange="{() => console.log('slide change')}"
                on:swiper="{(e) => console.log(e.detail[0])}">
                {#each navItems as item}
                    <SwiperSlide>
                        <a href="{item.link}" use:link class="nav-item-main">
                            <span class="nav-item-main-title"
                                >{item.title}</span>
                            <span class="nav-item-main-subtitle"
                                >{item.subtitle}</span>
                        </a>
                    </SwiperSlide>
                    
                    {#if item.subitems}
                        {#each item.subitems as subItem}
                            <SwiperSlide>
                                <a
                                    href="{subItem.link}"
                                    use:link
                                    class="nav-item-sub">
                                    <span class="nav-item-sub-title"
                                        >{subItem.title}</span>
                                    <span class="nav-item-sub-subtitle"
                                        >{subItem.subtitle}</span>
                                </a>
                            </SwiperSlide>
                        {/each}
                    {/if}
                    <hr>
                {/each}
            </Swiper>
        </div>
    </div>
</nav>
