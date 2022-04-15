<script lang="ts">
  import 'temporal-polyfill/global'

  let time = Temporal.Now.plainTimeISO()

  $: timeString = time.toLocaleString()

  setInterval(() => {
    time = Temporal.Now.plainTimeISO()
  }, 100)

</script>

<svelte:head>
<meta name="viewport" content="width=device-width, initial-scale=1">
</svelte:head>

<div>
  <h2>oclock</h2>
  <h1>{timeString}</h1>
</div>

<style>
@import url('https://fonts.cdnfonts.com/css/helvetica-neue-9');

h2,h1 {
  font-family: 'Helvetica Neue', sans-serif;
  text-align: center;
}
h2 {
  padding-top: 2rem;
}
h1 {
  font-size: 15rem;
  word-wrap: break-word;
}

div {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width:100%;
  height:100%;
}

@media (max-width: 950px) {
  h1 {
    font-size: 12rem;
  }
}
@media (max-width: 765px) {
  h1 {
    font-size: 9rem;
  }
}
@media (max-width: 580px) {
  h1 {
    font-size: 7rem;
  }
}

@media (max-width: 460px) {
  h1 {
    font-size: 5rem;
  }
}

@media (max-width: 374px) {
  h1 {
    font-size: 7rem;
  }
}

@media (max-width: 326px) {
  h1 {
    font-size: 7rem;
  }
}

@media (max-width: 460px) {
  h1 {
    font-size: 5rem;
  }
}

@media (max-width: 330px) {
  h1 {
    font-size: 5rem;
  }
}

@media (max-width: 310px) {
  h1 {
    font-size: 6rem;
  }
}

@media (max-width: 225px) {
  h1 {
    font-size: 7rem;
  }
}
</style>
