<script>
	const goBack = () => {
		window.location.href = '/'; // Redireciona para a página inicial
	};

	let amigos = [
		{
			nome: 'Ayla',
			imagem: 'ayla.jpeg',
			descricao:
				'Amores, essa é a Ayla! Essa garota é pura energia e tá sempre pronta pra uma nova aventura. Se tem algo divertido rolando, pode ter certeza que a Ayla tá lá, trazendo risadas e boas vibrações. Ela é aquele tipo de amiga que te levanta quando a coisa fica difícil e sempre tá do seu lado. Tô muito feliz de ter ela na minha vida e mal posso esperar pra compartilhar mais histórias nossas!!'
		},
		{
			nome: 'Mike, Lucio e Joto',
			imagem: 'mike.jpeg',
			descricao:
				'Esses aí são o Mike, o Lucio, e o Joto meus parceiros de todas as horas! O Mike é o rei das piadas, sempre fazendo a gente rir, e o Lucio é o Youtuber da turma, sempre gravando as nossas aventuras. Ah, e não posso esquecer de falar do Jotinho, ele é do Lucio e é uma fofura, sempre junto com a gente nas nossas aventuras. Com essa galera, a diversão garantida sempre!!'
		}
	];
</script>

<div class="container text-center">
	<h1 class="titulo-pagina">CLOSE FRIENDS</h1>
	<p class="subtitulo-pagina">Aqui vocês vão conhecer um pouco sobre meus melhores amigos</p>

	<div class="container-amigos">
		{#each amigos as amigo}
			<div class="container-cartao">
				<div class="cartao">
					<img src={amigo.imagem} alt={`Foto do ${amigo.nome}`} />
					<p>{amigo.descricao}</p>
				</div>
			</div>
		{/each}
	</div>

	<button class="btn-personalizado" on:click={goBack}> Voltar para a página inicial </button>
</div>

<style>
	.titulo-pagina {
		color: pink;
		font-size: 2.5rem;
		font-weight: bold;
		text-align: center;
		margin-top: 2rem;
	}

	.subtitulo-pagina {
		font-size: 1.2rem;
		text-align: center;
		margin-bottom: 2rem;
	}

	.cartao {
		background-color: pink;
		color: white;
		border-radius: 15px;
		padding: 1.5rem;
		margin: 2rem;
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		height: 550px;
		box-sizing: border-box;
	}

	.cartao img {
		width: 100%;
		height: 200px;
		object-fit: cover;
		border-radius: 15px;
		margin-bottom: 1rem;
	}

	.btn-personalizado {
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

	.btn-personalizado:hover {
		background-color: #ff85c2;
	}

	.container-amigos {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
	}

	.container-cartao {
		flex: 1 1 45%;
		max-width: 400px;
		display: flex;
		justify-content: center;
	}
</style>
