<script>
  import { register, init, getLocaleFromNavigator, _, isLoading } from 'svelte-i18n';
 
  register("en", () => import('./i18n/en.json'));

  init({
    fallbackLocale: 'en',
    initialLocale: getLocaleFromNavigator(),
  });
  import Home from './pages/home.svelte'
</script>

{#if $isLoading}
 <div class="loading">Loading...</div>
{:else}
<Home/>
{/if}

<style>
  .loading {
    align-items: center;
  }
</style>
