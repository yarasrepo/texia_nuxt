<template>
    <div class="container">
        <img src="/images/signin_image.png" alt="signin_image">
        <div class="right_container">
            <div class="sign_in_container">
                <div class="logo">
                    <img src="/img/logo.png" alt="logo" class="logo-image">
                </div>
                <div class="account_text">
                    <h1 class="welcome_text">Welcome back to Texia,<br>sign in to continue</h1>
                    <h4 class="account_text_small">Don't have an account? <a href="#">Create new account</a><br>It
                        takes less than a minute</h4>
                </div>

                <div class="input_container">
                <UForm :state="state" :schema="schema" ref="form" @submit.prevent="save">
                    <UFormGroup name="email" class="mb-8">
                        <label class= "prof_email_add">Professional email address</label><br>
                        <UInput type="email" icon="i-mage-email" v-model="state.email"  />
                        <!-- class="bg-gray-100 w-[608px] h-[43px] rounded-[8px] p-[11px 14px] mb-30" -->
                    </UFormGroup>

                    <!-- <div class="input_box_2"> -->
                    <UFormGroup>
                        <UInput type="password" icon="i-mage-lock" name="password" v-model="state.password" />
                    </UFormGroup>
                </UForm>

                </div>
                <a href="#">Recover Password</a><br>

                <UButton type="submit" icon="i-mage-arrow-right" />
            </div>
        </div>
    </div>
</template>

<script setup>
import {z} from 'zod'

const schema = z.object({
    email: z.string().email('Invalid email'),
    password: z.string().min(8, 'Must be at least 8 characters')
})

const form= ref()

const save = async ()=> {
    form.value.validate()
}

const initialState = {
    type: undefined,
    email: undefined,
    password: undefined
}

const state= ref({
    ...initialState
})

const resetForm = () => {
    Object.assign(state.value, initialState)
}

// const isOpen = computed({
//     get: () => props.modelValue,
//     set: (value) => {
//         if (!value) resetForm()
//         emit(event: 'update:modeValue', value)
//     }
// })
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

.container img {
    height: 100%;
    border-radius: 12px;
}

.right_container {
    padding: 40px;
    flex-grow: 1;
}

.sign_in_container {
    text-align: center;
    width: 608px;
    height: 546px;
    margin: 50px;
}

.logo {
    position: relative;
    width: 80px;
    height: 81px;
    background-color: #100F73;
    border-radius: 50%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}

.logo-image {
    width: 60px;
    height: 60px;
    object-fit: cover;
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

/* .prof_email_add {
    font-size: 12px;
    font-weight: 700;
    color: #6A6C77;
    float: left;
} */

/* .input_box,
.input_box_2 {
    background-color: #F5F5FA;
    width: 608px;
    height: 43px;
    border-radius: 8px;
    padding: 11px 14px 11px 14px;
    margin-bottom: 30px;
} */

.input_box svg,
.input_box_2 .lock_icon {
    float: left;
}

.eye_closed_icon {
    float: right;
}

a {
    color: #4949AC;
}

.next_button {
    background-color: #4949AC;
    width: 300px;
    height: 48px;
    padding: 12px 24px 12px 24px;
    border-radius: 100px;
    margin-top: 30px;
    border: none;
}

.next_button svg {
    margin-left: 40px;
}
</style>