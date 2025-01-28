<script>
  // Função para voltar à página inicial
  const goBack = () => {
    window.location.href = "/"; // Redireciona para a página inicial
  };
</script>

<style>
  .page-title {
    color: pink;
    font-size: 2.5rem;
    font-weight: bold;
    text-align: center;
    margin-top: 2rem;
  }

  .page-subtitle {
    font-size: 1.2rem;
    text-align: center;
    margin-bottom: 2rem;
  }

  .card {
    background-color: pink;
    color: white;
    border-radius: 15px;
    padding: 1.5rem;
    margin: 2rem;
    text-align: center;
  }

  .card img {
    width: 100%;
    border-radius: 15px;
    margin-bottom: 1rem;
  }

  .btn-custom {
    background-color: pink;
    color: white;
    border: none;
    font-weight: bold;
    padding: 0.8rem 1.5rem;
    border-radius: 8px;
    margin: 1rem auto;
    cursor: pointer;
    transition: background-color 0.3s;
    display: block;
  }

  .btn-custom:hover {
    background-color: #ff85c2;
  }

  .friends-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
  }

  .card-container {
    flex: 1 1 45%;
    max-width: 400px;
  }
</style>

<div class="container text-center">
  <h1 class="page-title">CLOSE FRIENDS</h1>
  <p class="page-subtitle">Aqui vocês vão conhecer um pouco sobre meus melhores amigos</p>

  <div class="friends-container">
    <!-- Ayla -->
    <div class="card-container">
      <div class="card">
        <img src="ayla.jpeg" alt="Foto da Ayla">
        <p>
          Amores, essa é a Ayla! Essa garota é pura energia e tá sempre pronta
          pra uma nova aventura. Se tem algo divertido rolando, pode ter
          certeza que a Ayla tá lá, trazendo risadas e boas vibrações. Ela é
          aquele tipo de amiga que te levanta quando a coisa fica difícil e
          sempre tá do seu lado. Tô muito feliz de ter ela na minha vida e mal
          posso esperar pra compartilhar mais histórias nossas!!
        </p>
      </div>
    </div>

    <!-- Mike, Lucio e Joto -->
    <div class="card-container">
      <div class="card">
        <img src="mike.jpeg" alt="Foto do Mike, Lucio e Joto">
        <p>
          Esses aí são o Mike, o Lucio, e o Joto meus parceiros de todas as
          horas! O Mike é o rei das piadas, sempre fazendo a gente rir, e o
          Lucio é o Youtuber da turma, sempre gravando as nossas aventuras. Ah,
          e não posso esquecer de falar do Jotinho, ele é do Lucio e é uma
          fofura, sempre junto com a gente nas nossas aventuras. Com essa
          galera, a diversão garantida sempre!!
        </p>
      </div>
    </div>
  </div>

  <button class="btn-custom" on:click={goBack}>
    Voltar para a página inicial
  </button>
</div>