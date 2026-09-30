<script setup>
    import { ref } from 'vue';

    import MainNavigation from './components/MainNavigation.vue';
    import SiteFooter from './components/SiteFooter.vue';
    import SiteContent from './components/SiteContent.vue';
    import InputField from './components/InputField.vue';

    const title = ref('VUE')

    setTimeout(() => {
        title.value = 'REACT'
    }, 3000);

    function submitForm() {
        console.log('Form submitted:', formData);
    }

    const formData = reactive({ 
            email: '',
            firstName: '',
            lastName: ''
    });

</script>

<template>
    <header>
        <MainNavigation :title="title" />
        <!-- <MainNavigation /> -->
    </header>

    <main>
        <SiteContent />
        <!-- email input -->
        <InputField
            v-model="formData.email"
            id="e-mail"
            type="email"
            placeholder="Enter your e-mail"
            label="Email adress: "
        />

<!-- first name input -->

        <InputField
            v-model="formData.firstName"
            id="firstname"
            type="text"
            placeholder="Enter your first name"
            label="First name"
        />

        <!-- last name input -->

        <InputField
            v-model="formData.lastName"
            id="lastname"
            type="text"
            placeholder="Enter your last name"
            label="Last name: "
        />

        <button 
  
        @click="submitForm">Submit</button>

    </main>


    <footer>
        <!-- sitefooter komponens használata -->
        <SiteFooter />
    </footer>

</template>

<style scoped>
</style>
