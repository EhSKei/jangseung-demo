<script>
    import { onMount } from "svelte";
    import gsap from "gsap";

    let posterHue = 0;

    function checkTime() {
        let vid = document.getElementsByTagName("video")[0];
        let back = document.getElementsByTagName("img")[0];
        let c = document.getElementsByTagName("circle")[0];

        if (vid.currentTime < 6) {
            gsap.to(".poster-back", { filter: "hue-rotate(0deg)" });
            gsap.to("circle", {
                cx: -27.5,
                cy: 50,
                duration: 1,
                ease: "power4.out",
            });
        } else if (vid.currentTime < 13) {
            gsap.to(".poster-back", { filter: "hue-rotate(94deg)" });
            gsap.to("circle", {
                cx: 2.5,
                cy: 40,
                duration: 1,
                ease: "power4.out",
            });
        } else if (vid.currentTime < 20) {
            gsap.to(".poster-back", { filter: "hue-rotate(24deg)" });
            gsap.to("circle", {
                cx: 95,
                cy: 75,
                duration: 1,
                ease: "power4.out",
            });
        } else if (vid.currentTime < 27) {
            gsap.to(".poster-back", { filter: "hue-rotate(-75deg)" });
            gsap.to("circle", {
                cx: 97.5,
                cy: 30,
                duration: 1,
                ease: "power4.out",
            });
        } else if (vid.currentTime < 35) {
            gsap.to(".poster-back", { filter: "hue-rotate(-199deg)" });
            gsap.to("circle", {
                cx: 125,
                cy: 55,
                duration: 1,
                ease: "power4.out",
            });
        } else if (vid.currentTime < vid.duration) {
            gsap.to(".poster-back", { filter: "hue-rotate(0deg)" });
            gsap.to("circle", {
                cx: -27.5,
                cy: 50,
                duration: 1,
                ease: "power4.out",
            });
        }
    }

    function resizeCanvas() {
        let c = document.getElementsByClassName("poster-container")[0];
        // @ts-ignore
        // @ts-ignore
        c.style.width = window.innerWidth + "px";
        // @ts-ignore
        c.style.height = window.innerHeight + "px";
        // @ts-ignore
        console.log(c.style.width);
    }

    onMount(() => {
        resizeCanvas();
        window.addEventListener("resize", resizeCanvas);

        let vid = document.getElementsByTagName("video")[0];

        setInterval(checkTime, 500);
    });
</script>

<section class="poster-container">
    <video
        src="./poster/poster.mp4"
        type="video/mp4"
        class="poster-video"
        id="posterVideo"
        loop
        muted
        autoplay
        playsinline></video>
    <img
        src="./poster/posterback.jpg"
        alt=""
        class="poster-back"
        style="hue-rotate({posterHue}deg)" />
    <svg
        viewBox="0 0 100 100"
        xmlns="http://www.w3.org/2000/svg"
        class="poster-circle">
        <circle cx="-25%" cy="-50%" r="20" fill="white"></circle>
    </svg>
</section>
