<script>
  import { goto } from '$app/navigation';
  import { onMount } from 'svelte';

  let mostrarPopup = false;
  let diasAtras = 0;

  function calcularDiasAteDataFutura() {
      const dataAtual = new Date();
      const dataFutura = new Date('2024-12-26');

      const diferencaMs = dataFutura - dataAtual;

      const diferencaDias = Math.abs(Math.floor(diferencaMs / (1000 * 60 * 60 * 24)));

      return diferencaDias;
  }

  onMount(() => {
      diasAtras = calcularDiasAteDataFutura();

      const intervalo = setInterval(() => {
          diasAtras = calcularDiasAteDataFutura();
      }, 1000);

      return () => clearInterval(intervalo);
  });
</script>

<style>
  .titulo-blog {
      color: pink;
      font-size: 2.5rem;
      font-weight: bold;
      text-align: center;
      margin-top: 2rem;
  }

  .card {
      background-color: pink;
      color: white;
      border-radius: 15px;
      padding: 1.5rem;
      margin: 2rem auto;
      max-width: 600px;
      text-align: center;
      position: relative;
  }

  .btn-personalizado {
      background-color: pink;
      color: white;
      border: none;
      font-weight: bold;
      padding: 0.8rem 1.5rem;
      border-radius: 8px;
      margin: 0.5rem;
      cursor: pointer;
      transition: background-color 0.3s;
  }

  .btn-personalizado:hover {
      background-color: #ff85c2;
  }

  .imagem-perfil {
      display: block;
      margin: 1rem auto;
      border-radius: 25%;
      width: 300px;
      height: 300px;
      object-fit: cover;
      border: 4px solid pink;
  }

  .container-botoes {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin-top: 1rem;
  }

  .popup {
      position: absolute;
      background-color: white;
      color: black;
      border: 1px solid #ccc;
      padding: 10px;
      border-radius: 5px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      z-index: 1000;
      max-width: 300px;
      text-align: left;
      top: 100%;
      left: 50%;
      transform: translateX(-50%);
  }

  .texto-interativo {
      cursor: pointer;
      text-decoration: underline;
  }
</style>

<div class="container text-center">
  <h1 class="titulo-blog">BLOG DA MEL</h1>

  <div class="card">
      <p>
          Oie divos e divas, eu sou a Melissa, faço parte do 
          <span 
              role="button" 
              tabindex="0" 
              class="texto-interativo" 
              on:mouseenter={() => mostrarPopup = true} 
              on:mouseleave={() => mostrarPopup = false}
          >
              <b>RPG Ordem Paranormal</b>
          </span> 
          e aqui vai um pouco de quem sou eu, sou extrovertida e, apesar de parecer uma pessoa presunçosa, eu me considero bastante simpática com os demais, inclusive tenho certa facilidade em formar conexões rápidas. Sempre sou carismática, confiante e extremamente vaidosa, sempre estando perfumada e bem vestida. 😉💋
          Minha primeira aparição no RPG foi há {diasAtras} dias atrás.
      </p>
      {#if mostrarPopup}
          <div class="popup">
              Ordem Paranormal é um universo ficcional e marca criada pelo streamer brasileiro Cellbit.<br><br>
              Atualmente, sua ramificação principal são os episódios de RPG de mesa exibidos aos sábados, às 18 horas, no canal do Cellbit na Twitch. Todas as terças ocorrem as reprises, ao mesmo horário e também na Twitch, e, às quintas-feiras, o episódio era publicado no canal Lives do Cellbit no YouTube. A partir de 2022, os episódios passaram a ser publicados no canal Ordem Paranormal.
          </div>
      {/if}
  </div>

  <img
      src="mel.jpeg"
      alt="Foto da Melissa"
      class="imagem-perfil"
  />

  <div class="container-botoes">
      <button class="btn-personalizado" on:click={() => goto('/close-friends')}>
          Close Friends
      </button>

      <button class="btn-personalizado" on:click={() => goto('/viagem')}>
          Viagem
      </button>
  </div>
</div>
