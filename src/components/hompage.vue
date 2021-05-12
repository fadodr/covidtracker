<template>
    <div class="container">
        <div>
            <Main />
            <Cliprect />
        </div>
        <Areas />
        <Spread />
        <Symptons />
        <symptonsec />
        <Faq />
        <Blog />
    </div>
</template>

<script>
import Main from './main'
import Cliprect from './cliprect'
import Areas from './areas'
import Spread from './spread'
import Symptons from './symptons'
import Symptonsec from './symptonssec'
import Faq from './faq'
import Blog from './blog'
export default {
    components : {
        Main,
        Cliprect,
        Areas,
        Spread,
        Symptons,
        Symptonsec,
        Faq,
        Blog,
    }
}
</script>

<style scoped>

</style>