<template>
  <div class="card">
    <h2 class="card__title">Traffic Runners, LLC</h2>
    <p class="card__subtitle">Softwear company</p>

    <div class="tabs">
      <div class="tabs__wrapper">
        <div class="tabs__label-wrapper tabs__label-wrapper--standard">
          <input
            class="visually-hidden"
            type="radio" id="standard" name="tab"
            :checked="(activeTab === 'standard') ? true : false"
            :disabled="tabs['standard'].disabled"
            @click="changeTab('standard')">
          <label for="standard">
            <span>
              <svg xmlns="http://www.w3.org/2000/svg" width="17" height="22" viewBox="0 0 17 22">
                <path fill="#FFF" d="M14.875 0C16.048 0 17 .924 17 2.063v17.875C17 21.075 16.048 22 14.875 22H2.125C.952 22 0 21.076 0 19.937V2.063C0 .925.952 0 2.125 0h12.75zm-4.423 17.27H3.4l-.114.007c-.447.054-.793.424-.793.873 0 .486.406.88.907.88h7.052l.114-.007c.447-.054.793-.424.793-.873 0-.486-.406-.88-.907-.88zm3.022-3.3H3.4l-.114.007c-.447.054-.793.424-.793.873 0 .486.406.88.907.88h10.074l.114-.007c.447-.054.793-.424.793-.873 0-.486-.406-.88-.907-.88zm-2.015-3.3H3.4l-.114.007c-.447.054-.793.424-.793.873 0 .486.406.88.907.88h8.06l.113-.007c.447-.054.793-.424.793-.873 0-.486-.406-.88-.907-.88zM7.933 2.42H3.4l-.114.007c-.447.054-.793.424-.793.873 0 .486.406.88.907.88h4.533l.114-.007c.447-.054.793-.424.793-.873 0-.486-.406-.88-.907-.88z"/>
              </svg>
            </span>
            <span>Standard</span>
            </label>
        </div>
        <div class="tabs__label-wrapper tabs__label-wrapper--event">
          <input
            class="visually-hidden" type="radio" id="event" name="tab"
            :checked="(activeTab === 'event') ? true : false"
            :disabled="tabs['event'].disabled"
            @click="changeTab('event')">
          <label for="event">
            <span>
              <svg xmlns="http://www.w3.org/2000/svg" width="19" height="22" viewBox="0 0 19 22">
                <path fill="#77838F" d="M6.277 12.375H4.58c-.28 0-.509-.232-.509-.516v-1.718c0-.284.23-.516.51-.516h1.696c.28 0 .509.232.509.516v1.718c0 .284-.23.516-.51.516zm4.58-.516v-1.718c0-.284-.229-.516-.509-.516H8.652c-.28 0-.51.232-.51.516v1.718c0 .284.23.516.51.516h1.696c.28 0 .51-.232.51-.516zm4.072 0v-1.718c0-.284-.23-.516-.51-.516h-1.696c-.28 0-.509.232-.509.516v1.718c0 .284.23.516.51.516h1.696c.28 0 .509-.232.509-.516zm-4.072 4.125v-1.718c0-.284-.229-.516-.509-.516H8.652c-.28 0-.51.232-.51.516v1.718c0 .284.23.516.51.516h1.696c.28 0 .51-.232.51-.516zm-4.071 0v-1.718c0-.284-.23-.516-.51-.516H4.58c-.28 0-.509.232-.509.516v1.718c0 .284.23.516.51.516h1.696c.28 0 .509-.232.509-.516zm8.143 0v-1.718c0-.284-.23-.516-.51-.516h-1.696c-.28 0-.509.232-.509.516v1.718c0 .284.23.516.51.516h1.696c.28 0 .509-.232.509-.516zM19 4.813v15.125C19 21.075 18.088 22 16.964 22H2.036C.912 22 0 21.076 0 19.937V4.813C0 3.675.912 2.75 2.036 2.75H4.07V.516c0-.284.23-.516.51-.516h1.696c.28 0 .509.232.509.516V2.75h5.428V.516c0-.284.23-.516.51-.516h1.696c.28 0 .509.232.509.516V2.75h2.035c1.124 0 2.036.924 2.036 2.063zM16.964 19.68V6.875H2.036V19.68c0 .141.114.258.254.258h14.42c.14 0 .254-.117.254-.258z"/>
              </svg>
            </span>
            <span>Event</span>
          </label>
        </div>
        <div class="tabs__label-wrapper tabs__label-wrapper--alert">
          <input
            class="visually-hidden" type="radio" id="alert" name="tab"
            :checked="(activeTab === 'alert') ? true : false"
            :disabled="tabs['alert'].disabled"
            @click="changeTab('alert')">
          <label for="alert">
            <span>
              <svg xmlns="http://www.w3.org/2000/svg" width="28" height="22" viewBox="0 0 28 22">
                <path fill="#77838F" d="M4.9 8.25c0-.57-.47-1.031-1.05-1.031h-2.8C.47 7.219 0 7.68 0 8.25c0 .57.47 1.031 1.05 1.031h2.8c.58 0 1.05-.461 1.05-1.031zM2.26 2.784l2.425 1.375c.325.192.73.197 1.06.012.33-.184.534-.53.531-.902-.002-.373-.209-.716-.541-.896L3.31.998C2.985.805 2.58.8 2.25.985c-.33.184-.534.53-.531.902.002.373.209.716.541.897zm20.531 1.513c.185 0 .366-.048.525-.138l2.425-1.375c.49-.29.654-.913.367-1.4-.286-.487-.916-.658-1.417-.386l-2.425 1.375c-.411.233-.612.709-.489 1.16.123.45.539.764 1.014.764zM14 22c1.546 0 2.8-1.231 2.8-2.75h-5.6c0 1.519 1.254 2.75 2.8 2.75zM26.95 7.219h-2.8c-.58 0-1.05.461-1.05 1.031 0 .57.47 1.031 1.05 1.031h2.8c.58 0 1.05-.461 1.05-1.031 0-.57-.47-1.031-1.05-1.031zm-5.953 1.718c0-3.338-2.384-6.011-5.598-6.667v-.895C15.4.615 14.772 0 14 0c-.773 0-1.4.616-1.4 1.375v.895c-3.212.656-5.596 3.33-5.596 6.668 0 4.396-1.58 5.737-2.426 6.629-.244.251-.379.586-.377.933.005.705.569 1.375 1.404 1.375h16.792c.836 0 1.4-.67 1.404-1.375.002-.347-.133-.682-.377-.933-.845-.892-2.426-2.233-2.426-6.63z"/>
              </svg>
            </span>
            <span>Alert</span>
          </label>
        </div>
      </div>

      <div class="tabs__content-wrapper">
        <div class="tabs__content standard" v-if="activeTab === 'standard'">
          <!-- Контент вкладки стандарт -->
          <form
            action="#"
            @submit="checkForm"
          >
            <div class="standard__input-wrapper">
              <label for="button-link">Link to the button</label>
              <input
                v-model="link"
                name="button-link"
                id="button-link"
                type="text"
              >
            </div>
            <p class="standard__text"> You can use any link, but it’s length should not exceed 200 characters</p>

            <p v-if="errors.length">
              <b>Пожалуйста исправьте указанные ошибки:</b>
              <ul>
                <li v-for="error in errors" :key="error">{{ error }}</li>
              </ul>
            </p>

            <button class="standard__submit" type="submit">Continue</button>
          </form>
        </div>

        <div class="tabs__content" v-if="activeTab === 'event'">
          Контент вкладки event
        </div>

        <div class="tabs__content" v-if="activeTab === 'alert'">
          <!-- Контент вкладки alert -->
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'SimpleBlock',
  data () {
    return {
      tabs: {
        standard: {
          disabled: false
        },
        event: {
          disabled: false
        },
        alert: {
          disabled: true
        }
      },
      activeTab: 'standard',
      errors: [],
      link: null
    }
  },
  methods: {
    changeTab (tab) {
      if (!this.tabs[tab].disabled) {
        this.activeTab = tab
      }
    },
    checkForm: function (e) {
      e.preventDefault()
      this.errors = []

      if (this.link.length >= 200) {
        this.errors.push('Длина ссылки превышает 200 символов.')
      }

      if (this.errors.length === 0) {
        console.log(this.link)
      }
    }
  }
}
</script>

<style scoped>
.card {
  width: 512px;
  min-height: 480px;
  margin: 0 auto;
  padding: 36px 25px 80px 32px;
  border-radius: 4px;
  box-shadow: 0 8px 8px 0 rgba(119, 131, 143, 0.16);
  background-color: #fff;
  box-sizing: border-box;
}
.card__title {
  margin: 0 2px 0 0;
  font-size: 24px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.11px;
  color: #000;
}
.card__subtitle {
  margin: 0 0 26px 0;
  font-size: 18px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.08px;
  color: #828e9a;
}
.tabs__wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 2px;
  border-radius: 24px;
  overflow: hidden;
  margin-bottom: 25px;
}
.tabs__label-wrapper label {
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 8px;
  position: relative;
  color: #77838f;
  background-color: #e7eaf3;
  padding: 8px 29px 9px 30px;
  font-size: 16px;
  font-weight: 600;
  line-height: 22px;
  letter-spacing: -0.07px;
}
.tabs__label-wrapper label:hover {
  opacity: 0.5;
}
.tabs__label-wrapper span {
  height: 22px;
}

.tabs__label-wrapper span svg path {
  fill: #77838f;
}

.tabs__label-wrapper input:checked + label span svg path {
  fill: #fff;
}
.tabs__label-wrapper input:checked + label {
  background-color: #377dff;
  color: #fff;
}
.tabs__label-wrapper input:disabled + label {
  opacity: 0.5;
}
.standard {
  padding: 8px;
}
.standard__input-wrapper {
  margin-bottom: 23px;
}
.standard__input-wrapper label {
  font-size: 18px;
  font-weight: 600;
  line-height: 1.44;
  letter-spacing: -0.08px;
  color: #77838f;
  margin: 5px 0;
}
.standard__input-wrapper input {
  display: block;
  width: 100%;
  padding: 12px 24px;
  box-sizing: border-box;
  font-family: 'Nunito', Helvetica, Arial, sans-serif;
  font-size: 16px;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: -0.07px;
  color: #77838f;
  border-radius: 24px;
  border: solid 1px rgba(119, 131, 143, 0.56);
  background-color: #fff;
}
.standard__input-wrapper input:hover {
    background-color: rgb(243, 241, 241);
}
.standard__text {
  font-size: 16px;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: -0.07px;
  color: #000;
  max-width: 383px;
}
.standard__submit {
  font-family: 'Nunito', Helvetica, Arial, sans-serif;
  font-size: 18px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: -0.08px;
  text-align: center;
  color: #fff;
  border-radius: 27.5px;
  border: none;
  padding: 7px 27px 9px 28px;
  background-color: #377dff;
}
.standard__submit:hover {
  opacity: 0.5;
}
</style>
