<template>
    <PageFirst text="Nosso pequeno time de profissionais internacionais vão te acompanhar em cada passo do projeto. Relacionamentos fortes são o núcleo de tudo que fazemos. Isso abrange o relacionamento que os nosso tem com o ambiente." subTitle="Nosso time de profissionais" title="Sobre" :img="require('@/assets/aboutImg1.svg')"/>
    <AboutHeritage/>
    <LeadersComponent/>
</template>

<script>
import PageFirst from '@/components/PageFirst.vue';
import AboutHeritage from '@/components/AboutHeritage.vue';
import LeadersComponent from '@/components/LeadersComponent.vue';
export default {
    name: 'AboutView',
    components:{
        PageFirst,
        AboutHeritage,
        LeadersComponent
    }
}
</script>