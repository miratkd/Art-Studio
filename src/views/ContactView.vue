<template>
    <PageFirst text="Nos adoraríamos ouvir sobre o seu projeto. Por favor, deixe uma mensagem abaixo ou nos ligue.Nos temos dois escritórios, um no Texas outro no Tennessee. Se estiver passando por la, venha nos dar um olá!" subTitle="Nos diga sobre o seu projeto" title="Contato" :img="require('@/assets/contactImg1.svg')"/>
    <ContactInfo/>
    <ContactImg/>
    <ContactForm/>
</template>

<script>
import PageFirst from '@/components/PageFirst.vue';
import ContactInfo from '@/components/ContactInfo.vue';
import ContactImg from '@/components/ContactImg.vue';
import ContactForm from '@/components/ContactForm.vue';
export default{
    name: 'ContactView',
    components:{
        PageFirst,
        ContactInfo,
        ContactImg,
        ContactForm
    }
}
</script>