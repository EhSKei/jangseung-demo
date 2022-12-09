<script>
    import { link } from "svelte-spa-router";

    import { Swiper, SwiperSlide } from "swiper/svelte";
    import { Mousewheel, Navigation } from "swiper";

    import "swiper/css";
    import "swiper/css/mousewheel";
    import "swiper/css/navigation";

    const navItems = [
        {
            title: "HOME",
            subtitle: "",
            link: "/",
            image: "./footer/footer01.jpg",
        },
        {
            title: "들어가는 글",
            subtitle: "왜 장승 솟대인가?",
            link: "/prologue",
            image: "./footer/footer02.jpg",
        },
        {
            title: "1부",
            subtitle: "젊은 민속학자들, 장승과 솟대를 조사하다.",
            link: "/chapter01",
            image: "./footer/footer03.png",
        },
        {
            title: "2부",
            subtitle: "한국 장승·솟대의 역사",
            link: "/chapter02",
            image: "./footer/footer04.png",

            subitems: [
                {
                    title: "2-1",
                    subtitle: "장승의 역사",
                    link: "/chapter02-1",
                },
                {
                    title: "2-2",
                    subtitle: "솟대의 역사",
                    link: "/chapter02-1",
                },
                {
                    title: "2-3",
                    subtitle: "장승과 솟대의 만남",
                    link: "/chapter02-1",
                },
            ],
        },
        {
            title: "3부",
            subtitle: "장승과 솟대의 존재 양상",
            link: "/chapter03",
            image: "./footer/footer05.jpg",
        },
        {
            title: "4부",
            subtitle: "전국의 장승·솟대를 조사하라!",
            link: "/chapter04",
            image: "./footer/footer01.jpg",

            subitems: [
                {
                    title: "1. 1988년, 서울 올림픽의 해",
                    subtitle: "경기도, 강원도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "2. 1989년, 장승·솟대 조사의 성숙기",
                    subtitle: "경상북도, 충청북도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "3. 1990년, 장승·솟대 조사의 성장기",
                    subtitle: "충청남도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "4. 1991~1995년, 장승·솟대 조사의 비약적 성장기",
                    subtitle: " 전라북도, 전라남도 조사",
                    link: "/chapter04-1",
                },
                {
                    title: "5. 1996~1997년, 장승·솟대 조사 피날레",
                    subtitle: "경상남도(제주도) 조사",
                    link: "/chapter04-1",
                },
            ],
        },
        {
            title: "끝내는 글",
            subtitle: "10년 동안의 기나긴 여정, 전국 장승·솟대조사 대작전",
            link: "/epilogue",
            image: "./footer/footer07.jpg",
        },
    ];
</script>

<footer class="footer">
    <Swiper
        slidesPerView="{'auto'}"
        spaceBetween="{20}"
        centeredSlides="{true}"
        grabCursor="{true}"
        modules="{[Mousewheel, Navigation]}"
        mousewheel
        navigation
        on:slideChange="{() => console.log('slide change')}"
        on:swiper="{(e) => console.log(e.detail[0])}"
        style="padding: 50px">
        {#each navItems as item}
            <SwiperSlide>
                <div class="footer-item-container">
                    <div class="footer-item-sub">
                        <div class="footer-item-sub-container">
                            <a
                                href="{item.link}"
                                use:link
                                on:click={()=>window.scrollTo(0,0)}
                                class="footer-item-link">
                                <span class="footer-item-sub-title"
                                    >{item.title}</span>
                                <hr />
                                <span class="footer-item-sub-subtitle"
                                    >{item.subtitle}</span>
                            </a>

                            {#if item.subitems}
                                {#each item.subitems as subItem}
                                    <a
                                        href="{subItem.link}"
                                        class="footer-item-link"
                                        use:link>
                                        <span class="footer-subitem-title">
                                            {subItem.title}
                                        </span>
                                        <span class="footer-subitem-subtitle"
                                            >{subItem.subtitle}</span>
                                    </a>
                                {/each}
                            {/if}
                        </div>
                    </div>
                    <div
                        class="footer-item-main"
                        style="background-image:url({item.image})">
                        <div class="footer-item-main-container">
                            <a
                                href="{item.link}"
                                use:link
                                class="footer-item-link">
                                <span class="footer-item-main-title"
                                    >{item.title}</span>
                                <hr />
                                <span class="footer-item-main-subtitle"
                                    >{item.subtitle}</span>
                            </a>
                        </div>
                    </div>
                </div>
            </SwiperSlide>
        {/each}
    </Swiper>
</footer>
