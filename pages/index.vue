<template>
    <div class="container">
        <img src="/images/signin_image.png" alt="signin_image" class="sign_in_image">
        <div class="right_container">
            <div class="sign_in_container">
                <img src="/img/logo.png" alt="logo" class="logo-image">
                <div class="account_text">
                    <h1 class="welcome_text">Welcome back to Texia,<br>sign in to continue</h1>
                    <h4 class="account_text_small">Don't have an account? <a href="#">Create new account</a><br>It
                        takes less than a minute</h4>
                </div>

                <UForm :state="state" :schema="schema" ref="form" @submit.prevent="save">
                    <UFormGroup name="email" class="mb-8">
                        <label id="prof_email_add">Professional email address</label><br>
                        <UInput type="email" icon="i-mage-email" v-model="state.email" :class="['input_box']"
                            id="email_field" />
                    </UFormGroup>
                    <UFormGroup class="form-box">
                        <UInput type="password" icon="i-mage-lock" name="password" v-model="state.password"
                            :class="['input_box']" id="email_field" />
                        <UIcon name="i-mage-eye-off" id="eye-icon" />
                    </UFormGroup>
                </UForm>

                <a href="#">Recover Password</a><br>

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

const resetForm = () => {
    Object.assign(state.value, initialState)
}
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

.sign_in_image {
    height: 100%;
    border-radius: 12px;
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
    font-weight: bold;
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

.input_box {
    background-color: #F5F5FA;
    width: 608px;
    height: 43px;
    border-radius: 8px;
    padding: 11px 14px 11px 14px;
    margin-bottom: 30px;
    padding-right: 40px;
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

#email_field {
    margin-top: -10px;
    padding: 10px 45px;
    margin-left: -14px;
    width: 608px;
}

a {
    color: #4949AC;
}

#next_button {
    background-color: #4949AC;
    width: 300px;
    height: 48px;
    padding: 12px 24px 12px 70px;
    border-radius: 100px;
    margin-top: 30px;
    border: none;
    justify-content: center;
    align-items: center
}</style>