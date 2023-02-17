https://vuejs.org/api/sfc-script-setup.html#typescript-only-features
https://stackblitz.com/edit/vue-js-dynamic-style-with-variables?file=src%2FApp.vue

https://stackoverflow.com/questions/47322875/vue-js-dynamic-style-with-variables


<template>
    <div class="class_name" :style="{'--bkgImage': 'url(' + project.background + ')', '--bkgImageMobile': 'url(' + project.backgroundRetina + ')'}">
    </div>
</template>

<style>
    .class_name{
        background-image: var(--bkgImage);
    }
    @media all and (-webkit-min-device-pixel-ratio : 1.5),
        all and (-o-min-device-pixel-ratio: 3/2),
        all and (min--moz-device-pixel-ratio: 1.5),
        all and (min-device-pixel-ratio: 1.5) {
            .class_name {
                background-image: var(--bkgImageMobile);
            }
        }
</style>



