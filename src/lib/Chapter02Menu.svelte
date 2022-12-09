<script>
    import { link } from "svelte-spa-router";
</script>

<main>
    <div class="menu-container">
        <div class="menu-item" style="background-image:url('./chapter02/003.webp')">
            <a href="/chapter02-1" use:link class="menu-link">
                <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" >
                    <circle cx="50%" cy="50%" r="50%" fill="none" ></circle>
                </svg>
                <span class="menu-text"> 장승의 역사 </span>
            </a>
        </div>
        <div class="menu-item" style="background-image:url('./chapter02/013.webp')">
            <a href="/chapter02-2" use:link class="menu-link">
                <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" >
                    <circle cx="50%" cy="50%" r="50%" fill="none" ></circle>
                </svg>
                <span class="menu-text"> 솟대의 역사 </span>
            </a>
        </div>
        <div class="menu-item" style="background-image:url('./chapter02/023.webp')">
            <a href="/chapter02-3" use:link class="menu-link">
                <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" >
                    <circle cx="50%" cy="50%" r="50%" fill="none" ></circle>
                </svg>
                <span class="menu-text"> 장승과 솟대의 만남 </span>
            </a>
        </div>
    </div>
</main>
