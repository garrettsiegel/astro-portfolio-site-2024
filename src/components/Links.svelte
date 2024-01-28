<script>
  import GithubIcon from '../components/logos/github.svelte'
  import CodepenIcon from '../components/logos/codepen.svelte'
  import BehanceIcon from '../components/logos/behance.svelte'
  import UpworkIcon from '../components/logos/upwork.svelte'
  import TwitterIcon from '../components/logos/twitter.svelte'

  const links = [
    { label: "Github", url: "https://github.com/garrettsiegel", Icon: GithubIcon, desc: "Visit my Github profile" },
    { label: "Codepen", url: "https://codepen.io/garrettsiegel/pens/public", Icon: CodepenIcon, desc: "Check out my Codepen pens" },
    { label: "Behance", url: "https://www.behance.net/gsiegel", Icon: BehanceIcon, desc: "Explore my projects on Behance" },
    { label: "Upwork", url: "https://www.upwork.com/freelancers/garrettsubmurged", Icon: UpworkIcon, desc: "View my profile on Upwork" },
    { label: "Twitter", url: "https://twitter.com/garrettDoesCode", Icon: TwitterIcon, desc: "Follow me on Twitter" }
  ]
</script>


<div class="links">
  <ul>
    {#each links as { label, url, Icon, desc }}
      <li class="link">
        <a href={url} target="_blank" rel="noopener noreferrer" aria-label={desc}>
          <svelte:component this={Icon} class="icon" />
          <span class="is-hidden">{label} Icon</span>
        </a>
      </li>
    {/each}
  </ul>
</div>

<!-- 
<style>
  .links ul {
    display: flex;
    align-items: center;
    list-style: none;
  }

  .link {
    width: 30px
  }

  .link + * {
    margin-left: 1rem;
  }

  .is-hidden {
    position: absolute;
    overflow: hidden;
    clip: rect(0 0 0 0);
    height: 0px;
    width: 0px;
    margin: -1px;
    padding: 0;
    border: 0;
  }
</style> -->

<style lang="sass">
  .links 
    ul 
      display: flex 
      align-items: center 
      list-style: none 
  .link 
    width: 30px 
    & + * 
      margin-left: 1rem 
  .is-hidden 
    position: absolute 
    overflow: hidden 
    clip: rect(0 0 0 0) 
    height: 0px 
    width: 0px 
    margin: -1px 
    padding: 0 
    border: 0
</style>