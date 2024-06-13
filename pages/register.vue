<template>
    <div class="container">
        <img src="/img/register_image.png" alt="register" class="register_image">
        <div class="right_container">
            <div class="sign_in_container">
                <img src="/img/logo.png" alt="logo" class="logo-image">
                <div class="account_text">
                    <h1 class="welcome_text">Get started with TEXIA</h1>
                    <h4 class="account_text_small">Already have an account? <NuxtLink to="/">Sign in</NuxtLink><br></h4>
                </div>

                <UForm :state="state" :schema="schema" ref="form" @submit.prevent="save">
                    <UFormGroup name="full-name">
                        <label id="prof_email_add" for="full-name">Full Name</label><br>
                        <UInput type="text" variant="none" icon="i-mage-user" id="input_box"  />
                    </UFormGroup>
                    <UFormGroup name="email">
                        <label id="prof_email_add" for="email">Professional email address</label><br>
                        <UInput type="email" variant="none" icon="i-mage-email" v-model="state.email" id="input_box" />
                    </UFormGroup>
                    <div class="phone-container">
                    <USelect v-model="country" variant="none" :options="countries" id="phone-selector"/>
                    <UInput type="tel" variant="none" id="phone-input"></UInput>
                    </div>
                </UForm>

                <UButton type="submit" icon="i-mage-arrow-right" id="next_button" />
            </div>
        </div>
    </div>
</template>

<script setup>
import { z } from 'zod'

const schema = z.object({
    email: z.string().email('Invalid email'),
    password: z.string().min(8, 'Must be at least 8 characters')
})

const form = ref()

const save = async () => {
    form.value.validate()
}

const initialState = {
    type: undefined,
    email: undefined,
    password: undefined
}

const state = ref({
    ...initialState
})

const countries = ['US', 'CA', 'FR']

const country = ref(countries[0])
</script>

<style>
@font-face {
    font-family: 'Satoshi';
    src: url('fonts/Satoshi-Variable.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'Satoshi';
    src: url('fonts/Satoshi-VariableItalic.ttf') format('truetype');
    font-weight: normal;
    font-style: italic;
}

body {
    font-family: 'Satoshi', sans-serif;
    background-color: #ffffff;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.italic {
    font-style: italic;
}

.container {
    padding: 12.64px;
    display: flex;
}

.register_image {
    height: 100%;
    border-radius: 12px;
    width: 584px;
    height: 731px;
}

.right_container {
    padding: 40px;
    flex-grow: 1;
}

.sign_in_container {
    text-align: center;
    /* width: 608px;
    height: 546px; */
    margin: 50px;
}

.logo-image {
    position: relative;
    width: 80px;
    height: 81px;
    background-color: #100F73;
    border-radius: 50%;
    overflow: hidden;
    margin: auto;
}

.account_text {
    margin-top: 20px;
    margin-bottom: 20px;
}

.welcome_text {
    font-size: 36px;
    font-weight: lighter;
    font-style: italic;
}

.account_text_small {
    font-size: 16px;
    font-weight: 400;
    color: #6A6C77;
    margin-top: 20px;
    margin-bottom: 20px;
}

#prof_email_add {
    font-size: 12px;
    font-weight: 700;
    color: #6A6C77;
    float: left;
}

#input_box {
    background-color: #F5F5FA;
    width: 608px;
    height: 43px;
    border-radius: 8px;
    padding: 11px 14px 11px 14px;
    margin-bottom: 30px;
    padding-right: 40px;
    outline: none;
}

.form-box {
    position: relative;
}

#eye-icon {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    color: #9d9b9b;
    font-size: 20px;
}

.phone-container {
    display: flex;
    justify-content: space-between;
}

#phone-input {
    width: 530px;
    height: 43px;
    background-color: #F5F5FA;
    margin-top: 10px;
}

#phone-selector {
    height: 43px;
    background-color: #F5F5FA;
    margin-top: 10px;
}

a {
    color: #4949AC;
    text-decoration: underline;
}

#next_button {
    background-color: #4949AC;
    width: 300px;
    height: 48px;
    padding: 12px 24px 12px 70px;
    border-radius: 100px;
    margin-top: 40px;
    border: none;
    justify-content: center;
    align-items: center
}

</style>