<template>
    <div>
        <p>{{ $t("message.greeting", { name})}}</p>
        <p>{{ $t("message.goodbye", { name})}}</p>
        <button @click="setLocale('en')">English</button>
        <button @click="setLocale('es')">Spanish</button>
        <button @click="setLocale('de')">German</button>
        <p>{{ $tc("notification", 1)}}</p>
        <p>{{ $tc("notification", 2)}}</p>
    </div>
</template>

<script>
export default {
name: "HelloI18n",
  data() {
    return {
      name: 'Alena'
    }
  },
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