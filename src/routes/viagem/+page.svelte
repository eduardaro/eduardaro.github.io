<script>
	const goBack = () => {
		window.location.href = '/';
	};
</script>

<div class="container mt-5">
	<h1 class="titulo-blog">Viagem</h1>
	<h2 class="text-center texto-rosa mb-4">Preparados para verem tudo da viagem?</h2>

	<div class="text-center mb-4">
		<img src="viagem.jpeg" alt="Foto do grupo" class="img-fluida" />
	</div>

	<div class="card card-personalizado mb-4">
		<div class="card-body texto-card">
			<p>
				Essa aí foi a única foto decente que conseguimos tirar antes do caos que foi. Fomos para o
				acampamento Lua da Benquerença na noite de Natal. Foi uma verdadeira loucura, mas a diversão
				foi garantida!
			</p>
			<p>
				Assim que chegamos, o Breno levou uns brinquedos de Natal e a gente começou a decorar tudo
				de um jeito bem improvisado. O Lucio se empolgou e pendurou as coisas nos lugares mais
				estranhos. Teve até uma estrela na cabeça do Joto e todo mundo riu 😂
			</p>
			<p>
				A Ayla ficou encarregada da comida, mas adivinha? Esqueceram o fogareiro! O Jorge teve uma
				ideia genial e achou uma churrasqueira perdida no acampamento. Depois de algumas tentativas
				(e muitas risadas do Mike), conseguimos acender o fogo e fazer um jantar delicioso.
			</p>
			<p>
				Depois desse "baquete", partimos para a contação de histórias de terror ao redor da
				fogueira. O Joto entrou na onda e começou a latir como se fosse o nosso cão guarda. Jotinho
				é d+! 🐕🔥
			</p>
			<p>
				A noite foi cheia de risadas e cantorias desafinadas com o violão da Ayla. O Jorge estava
				lá, todo empolgado tentando acompanhar os passos malucos do Lucio e, odeio admitir, mas não
				tinha como não rir!
			</p>
			<p>
				No final das contas, apesar do caos total, nos divertimos demais e criamos memórias
				incríveis. Essa viagem vai ser lembrada como uma das melhores noites de Natal que já
				tivemos!
			</p>
		</div>
	</div>

	<div class="container-botoes">
		<button class="btn-personalizado" on:click={goBack}> Voltar para a página inicial </button>
	</div>
</div>

<style>
	.titulo-blog {
		color: pink;
		font-size: 2.5rem;
		font-weight: bold;
		text-align: center;
		margin-top: 2rem;
	}

	.texto-rosa {
		color: pink;
	}

	.card-personalizado {
		background-color: #ffccf2;
		border-radius: 15px;
	}

	.img-fluida {
		width: 100%; /* Faz a imagem ter a largura igual à do contêiner */
		max-width: 100%; /* Garante que a imagem não ultrapasse o tamanho do contêiner */
		border-radius: 10px;
	}

	.container-botoes {
		display: flex;
		justify-content: center;
		gap: 1rem;
		margin-top: 1rem;
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
</style>

