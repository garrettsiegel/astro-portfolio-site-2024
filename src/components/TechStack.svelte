<script>
  import HTMLIcon from '../components/logos/html.svelte';
  import CSSIcon from '../components/logos/css.svelte';
  import JSIcon from '../components/logos/js.svelte';
  import ReactIcon from '../components/logos/react.svelte';
  import NextIcon from '../components/logos/next.svelte';
  import AstroIcon from '../components/logos/astro.svelte';
  import GSAPIcon from '../components/logos/gsap.svelte';
  import HugoIcon from '../components/logos/hugo.svelte';
  import HandlebarsIcon from '../components/logos/handlebars.svelte';
  import SASSIcon from '../components/logos/sass.svelte';
  import TailwindIcon from '../components/logos/tailwind.svelte';
  import ViteIcon from '../components/logos/vite.svelte';

  const icons = [
    { id: 'html', component: HTMLIcon },
    { id: 'css', component: CSSIcon },
    { id: 'js', component: JSIcon },
    { id: 'react', component: ReactIcon },
    { id: 'next', component: NextIcon },
    { id: 'astro', component: AstroIcon },
    { id: 'gsap', component: GSAPIcon },
    { id: 'hugo', component: HugoIcon },
    { id: 'handlebars', component: HandlebarsIcon },
    { id: 'sass', component: SASSIcon },
    { id: 'tailwind', component: TailwindIcon },
    { id: 'vite', component: ViteIcon },
  ];


</script>

<style lang="sass">
  .current-tech
    margin-block: 1rem
</style>

<div class="module current-tech">
  <h2 class="current-tech__headline">Current Front End Technologies</h2>
  <div class="current-tech__skills">
    {#each icons as { component: Icon }}
      <div class="current-tech__skill">
        <svelte:component this={Icon} />
      </div>
    {/each}
  </div>
</div>
