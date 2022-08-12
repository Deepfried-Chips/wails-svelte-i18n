<script>
  import { addMessages, init, getLocaleFromNavigator, _ } from 'svelte-i18n';
  import en from './i18n/en.json';


  addMessages('en', en);

  init({
    fallbackLocale: 'en',
    initialLocale: getLocaleFromNavigator(),
  });
  import Home from './pages/home.svelte'
</script>

<Home/>
