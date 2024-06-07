<template>
    <div class="container">
        <img src="assets/image.png" alt="sign_in_image">
        <div class="right_container">
            <div class="sign_in_container">
                <div class="logo">
                    <svg width="80" height="81" viewBox="0 0 80 81" fill="none" xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink">
                        <circle cx="40" cy="40.7344" r="40" fill="#100F73" />
                        <rect x="10" y="10.7344" width="60" height="60" fill="url(#pattern0_4205_126743)" />
                        <mask id="mask0_4205_126743" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="10" y="10"
                            width="60" height="61">
                            <rect x="10" y="10.7344" width="60" height="60" fill="url(#pattern1_4205_126743)" />
                        </mask>
                        <g mask="url(#mask0_4205_126743)">
                            <path
                                d="M10 32.957H30.5556L33.3333 45.1793L36.1111 40.1793L31.6667 32.957H34.4444L37.7778 37.957L39.1667 32.957H43.3333V48.5126H40.5556L37.7778 42.957L34.4444 48.5126H10V32.957Z"
                                fill="white" />
                        </g>
                        <defs>
                            <pattern id="pattern0_4205_126743" patternContentUnits="objectBoundingBox" width="1"
                                height="1">
                                <use xlink:href="#image0_4205_126743"
                                    transform="translate(-0.0555556 -0.0694444) scale(0.00324886)" />
                            </pattern>
                            <pattern id="pattern1_4205_126743" patternContentUnits="objectBoundingBox" width="1"
                                height="1">
                                <use xlink:href="#image0_4205_126743"
                                    transform="translate(-0.0555556 -0.0694444) scale(0.00324886)" />
                            </pattern>
                            <image id="image0_4205_126743" width="342" height="342"
                                xlink:href="data:image/png;base64,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YgybTHUFAyuRG6ULMhDOMLXop8CS2nQ4YyTYDpdb8gQ8h0zPKGcDLCVlpepN+T1eQlPw/WQcF7WnMLASeREZC3Z8HzjBIVLhNF7qyY+DGZAk0jY2zmm9Wr6+KrVjz8IX+hRb0lZzyMTYYGAlioa1fxwCu2lfODgCPrUXwlJLbynTvMkUH/RB9zHNvcrkzF4tp/c6eayQ9/Q2/PpTDJqyEdQtGFiJom3VojTYaX2gnAJYQQmsqgCOMs2ihsurwyXQDpD0caRkuanoLA0zZkG1LHwpZcBbIs8dmMn4ymRdCRrDJRiztpw9oXoGAytRT6pYlIe6lJEt1mmkwB/OQsje2mp7X7gKA79ax4BJREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREREnv0/44IE6rn/R+kAAAAASUVORK5CYII=" />
                        </defs>
                    </svg>
                </div>
                <div class="account_text">
                    <h1 class="welcome_text">Welcome back to Texia,<br>sign in to continue</h1>
                    <h4 class="account_text_small">Don't have an account? <a href="#">Create new account</a><br>It
                        takes less than a minute</h4>
                </div>

                <div class="input_container">
                    <label class="prof_email_add">Professional email address</label><br>
                    <div class="input_box">
                        <svg width="20" height="21" viewBox="0 0 20 21" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M14.9178 7.61035L11.2151 10.6212C10.5155 11.1762 9.53122 11.1762 8.83164 10.6212L5.09766 7.61035"
                                stroke="#6A6C77" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
                            <path fill-rule="evenodd" clip-rule="evenodd"
                                d="M14.0901 17.7343C16.6245 17.7414 18.3327 15.659 18.3327 13.0997V7.37605C18.3327 4.81673 16.6245 2.73438 14.0901 2.73438H5.90863C3.37417 2.73438 1.66602 4.81673 1.66602 7.37605V13.0997C1.66602 15.659 3.37417 17.7414 5.90863 17.7343H14.0901Z"
                                stroke="#6A6C77" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </div>

                    <div class="input_box_2">
                        <svg class="lock_icon" width="20" height="21" viewBox="0 0 20 21" fill="none"
                            xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M13.6848 8.10709V6.31793C13.6848 4.22376 11.9865 2.52543 9.89232 2.52543C7.79815 2.51626 6.09315 4.20626 6.08398 6.30126V6.31793V8.10709"
                                stroke="#6A6C77" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
                            <path fill-rule="evenodd" clip-rule="evenodd"
                                d="M13.0685 17.942H6.70102C4.95602 17.942 3.54102 16.5279 3.54102 14.782V11.2079C3.54102 9.46202 4.95602 8.04785 6.70102 8.04785H13.0685C14.8135 8.04785 16.2285 9.46202 16.2285 11.2079V14.782C16.2285 16.5279 14.8135 17.942 13.0685 17.942Z"
                                stroke="#6A6C77" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
                            <path d="M9.88542 12.0693V13.9202" stroke="#6A6C77" stroke-width="1.5"
                                stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                        <svg class="eye_closed_icon" width="20" height="21" viewBox="0 0 20 21" fill="none"
                            xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M17 16.4844L4.5 3.98438M8.5 8.93569C8.18882 9.27876 8 9.7294 8 10.223C8 11.2978 8.89543 12.1691 10 12.1691C10.5093 12.1691 10.9741 11.9839 11.3272 11.6789M17.0323 12.1691C17.7209 11.1384 18 10.2978 18 10.2978C18 10.2978 16.1795 4.48438 10 4.48438C9.65308 4.48438 9.31989 4.5027 9 4.53729M14.5 14.6922C13.3521 15.4245 11.8744 15.9423 10 15.9117C3.89744 15.8119 2 10.2978 2 10.2978C2 10.2978 2.88155 7.48277 5.5 5.77047"
                                stroke="#6A6C77" stroke-width="1.5" stroke-linecap="round" />
                        </svg>
                    </div>
                </div>
                <a href="#">Recover Password</a><br>

                <button class="next_button">
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M4.25 12.7344H20.75" stroke="white" stroke-width="1.5" stroke-linecap="round"
                            stroke-linejoin="round" />
                        <path d="M14 5.98438L20.75 12.7344L14 19.4844" stroke="white" stroke-width="1.5"
                            stroke-linecap="round" stroke-linejoin="round" />
                    </svg>

                </button>
            </div>
        </div>
    </div>
</template>

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

.container img{
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

.prof_email_add {
    font-size: 12px;
    font-weight: 700;
    color: #6A6C77;
    float: left;
}

.input_box,
.input_box_2 {
    background-color: #F5F5FA;
    width: 608px;
    height: 43px;
    border-radius: 8px;
    padding: 11px 14px 11px 14px;
    margin-bottom: 30px;
}

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

.next_button svg{
    margin-left: 40px;
}
</style>