<template>
    <div>
        <p>{{ $t("message.greeting")}}</p>
        <p>{{ $t("message.goodbye")}}</p>
        <button @click="setLocale('en')">English</button>
        <button @click="setLocale('es')">Spanish</button>
        <button @click="setLocale('de')">German</button>
    </div>
</template>

<script>
export default {
  name: "HelloI18n",
  methods:{
    setLocale(locale) {
      this.$i18n.locale = locale;
      localStorage.setItem("locale", locale);
    }
  }
}
</script>
<style>
    button {
        margin: 10px;
        padding: 10px 20px;
        border: 2px solid plum;
        border-radius: 8px;
        background-color: white;
    }
</style>