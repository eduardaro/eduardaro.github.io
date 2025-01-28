<script>
    import { goto } from '$app/navigation'; // Importe a função goto para navegação programática
</script>
  
<style>
    .blog-title {
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
    }
  
    .btn-custom {
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
  
    .btn-custom:hover {
      background-color: #ff85c2;
    }
  
    .profile-image {
      display: block;
      margin: 1rem auto;
      border-radius: 25%;
      width: 150px;
      height: 150px;
      object-fit: cover;
      border: 4px solid pink;
    }
  
    .button-container {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin-top: 1rem;
    }
</style>
  
  <div class="container text-center">
    <h1 class="blog-title">BLOG DA MEL</h1>
  
    <div class="card">
      <p>
        Oie divos e divas, eu sou a Melissa e aqui vai um pouco de quem sou eu,
        sou extrovertida e, apesar de parecer uma pessoa presunçosa, eu me
        considero bastante simpática com os demais, inclusive tenho certa
        facilidade em formar conexões rápidas. Sempre sou carismática,
        confiante e extremamente vaidosa, sempre estando perfumada e bem
        vestida. 😉💋
      </p>
    </div>
  
    <img
      src="mel.jpeg"
      alt="Foto da Melissa"
      class="profile-image"
    />
  

    <div class="button-container">
        <button class="btn-custom" on:click={() => goto('/close-friends')}>
            Close Friends
        </button>

        <button class="btn-custom" on:click={() => goto('/viagem')}>
            Viagem
        </button>
    </div>
</div>