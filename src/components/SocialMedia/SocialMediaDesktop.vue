<template>
    <div class="about__card">
        <div class="about__social">
            <a class="icon about__social-github" target="_blank" href="https://github.com/KingYano">
                <i class="ri-github-line"></i>
            </a>
        </div>
        <div class="about__social">
            <a class="icon about__social-linkedin" target="_blank" href="https://www.linkedin.com/in/yanis-belkadi-746727209/">
                <i class="ri-linkedin-line"></i>
            </a>
        </div>
        <div class="about__social">
            <a class="icon about__social-mailto" target="_blank" href="mailto:belkadi.yanis.l@gmail.com">
                <i class="ri-mail-send-line"></i>
            </a>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss">
    .about__card {
        width: 50px;
        height: 200px;
        background-color: var(--banner-header-color);
        border-radius: var(--extra-boder-radius);
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;

        .about__social {
            width: 32px;
            height: 32px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 12px;
            background: var(--icon-social-color);

            .icon {
                color: var(--first-color);
            }
            &-github {

            }

            &-linkedin {

            }

            &-mailto {

            }
        }
    }
</style>
