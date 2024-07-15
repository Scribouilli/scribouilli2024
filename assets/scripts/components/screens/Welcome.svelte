<script>
  import Skeleton from "../Skeleton.svelte";

  export let showWelcome = false;
  export let isFetchingCurrentUserRepos = false;
</script>

<Skeleton>
  <section class="screen" id="welcome">
    {#if showWelcome}
       <h2>Le Nouveau Front Populaire a gagné, youpi !</h2>
      <p>Scribouilli 2024 se ferme donc, si vous voulez l'utiliser pour créer un petit site pour votre association, c'est possible sur <a href="https://atelier.scribouilli.org/">https://atelier.scribouilli.org/</a></p>

      <a href="https://atelier.scribouilli.org/" class="btn">Aller sur Scribouilli</a>
    {:else if isFetchingCurrentUserRepos }
      <h2>Nous regardons si vous avez plusieurs sites Scribouilli…</h2>
      <img
        src="./assets/images/hearts.svg"
        alt="cœur sur toi le temps que ça charge"
      />
    {/if}
  </section>
</Skeleton>
