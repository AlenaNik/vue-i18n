<template>
    <div>
        <p>{{ $t("message.greeting", { name})}}</p>
        <p>{{ $t("message.goodbye", { name})}}</p>
        <button @click="setLocale('en')">English</button>
        <button @click="setLocale('es')">Spanish</button>
        <button @click="setLocale('de')">German</button>
        <p>{{ $tc("notification", 1)}}</p>
        <p>{{ $tc("notification", 2)}}</p>
        <h1>{{$d(new Date(), "short")}}</h1>

<!--        <h1>{{$d(new Date(), "long")}}</h1>-->
        <br>
        <h1>Currency</h1>
        <p>{{$n(100, 'currency')}}</p>

       <p> {{ product }}</p>

        <button @click="setLocale('en-US')">USD</button>
        <button @click="setLocale('en-GB')">GBP</button>
        <button @click="setLocale('es-ES')">EUR</button>

    </div>
</template>

<script>
const products = {
   'en-GB': {
       name: 'Red jeans',
       stock: 4,
       price: 89
   },
   'en-US': {
       name: 'Red jeans',
       stock: 2,
       price: 109
    },
    'es-ES': {
        name: 'Vaqueros',
        stock: 2,
        price: 5
    },
}

export default {
name: "HelloI18n",
  data() {
    return {
      name: 'Alena'
    }
  },
  computed: {
    product() {
        return products[this.$i18n.locale];
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