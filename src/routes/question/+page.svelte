<!-- src/routes/index.svelte -->
<script>
	import { confetti } from '@neoconfetti/svelte';
	import { reduced_motion } from './reduced-motion';
	import { java } from '@codemirror/lang-java';
	import { cpp } from '@codemirror/lang-cpp';
	import { python } from '@codemirror/lang-python';
	import { dracula } from 'thememirror';
	import CustomCodeMirror from './CustomCodeMirror.svelte';
	let questionBody = `
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia voluptatem distinctio tempora
			molestiae! Maiores eaque perspiciatis libero voluptas quod quidem laborum commodi ratione?
			Repellat atque, architecto vero assumenda, totam aliquam saepe enim, ducimus facere dolores
			laboriosam consequatur magni! Explicabo veniam culpa repudiandae, perspiciatis nobis
			distinctio voluptatem eum reprehenderit repellendus incidunt ad facere autem accusamus
			excepturi impedit sapiente eveniet libero optio tenetur esse quis. Ducimus ipsa quia enim ex
			culpa, in eum illum ea suscipit deserunt placeat quos incidunt sed totam neque ab
			reprehenderit quo libero modi? Vitae eum impedit exercitationem, debitis pariatur voluptas
			aliquid consequuntur dolor, sapiente cumque quod quidem, sequi est et libero. Iusto, ipsum
			delectus atque quidem a quis quibusdam similique perspiciatis quaerat inventore tempora
			sapiente unde nemo animi? Quam ab quibusdam molestias odio quo, fugit error eius consequuntur
			dolor beatae dolore aliquam praesentium culpa? Adipisci incidunt ipsa eum reiciendis nihil
			maiores facilis voluptates hic, soluta magni labore necessitatibus maxime neque qui natus
			dolorem impedit velit earum beatae pariatur recusandae, aliquam tempore optio? Aspernatur,
			fuga unde vitae nam sint a, quam soluta autem iste ea illum voluptatem. Ad, repudiandae ea.
			Enim labore quas odio totam porro, possimus aperiam repudiandae nostrum recusandae placeat
			ratione sequi tenetur dolore cupiditate tempora dolor vero iusto, laudantium libero eius optio
			eos laborum. Officiis commodi minus ipsum placeat odio, debitis vitae a cum quasi doloremque
			eaque provident ex. Tenetur dolorum quo fuga, sed ab hic dicta reiciendis ipsa modi aspernatur
			doloremque enim nam eveniet, aliquid aperiam expedita voluptas laborum eaque adipisci. Beatae
			qui porro blanditiis architecto aspernatur maxime culpa quisquam, nam itaque officiis quia
			accusamus quas ipsa nesciunt corporis eius voluptatibus. Quis eos iure maxime illum, aut
			temporibus reiciendis facere magni hic suscipit cum, provident, similique ducimus minima
			deleniti eligendi expedita? Nobis vel facere provident optio neque tenetur, saepe et
			praesentium modi, culpa mollitia, eligendi quas laudantium atque dolores impedit sapiente quo
			nulla cum nihil aperiam placeat. Earum in amet doloribus nostrum architecto quae natus
			recusandae excepturi! Nemo dolorum, dolor ullam minima mollitia odit voluptatem commodi
			temporibus facilis et repudiandae quas nulla molestiae eaque obcaecati amet consectetur!
			Architecto esse quaerat neque. Corrupti asperiores architecto nihil tenetur obcaecati
			doloribus illum itaque voluptatibus laborum enim reiciendis cupiditate id, dolorum quibusdam
			similique, facere possimus aliquid facilis pariatur? Eius nemo sunt expedita omnis magnam, sed
			voluptatibus impedit aliquid molestias illum nihil totam id mollitia hic possimus
			necessitatibus saepe velit eos consequuntur repellat error! Quia dolores beatae possimus
			asperiores? Obcaecati, nisi. Veritatis autem reiciendis dolorum commodi voluptates officia,
			laudantium molestiae iure maxime fuga labore dolorem excepturi culpa nemo enim libero animi
			cum odio voluptatibus tempore. Aperiam dignissimos laudantium ad placeat vitae esse, adipisci
			libero! Illum magni modi dicta dignissimos sed voluptatem voluptatum provident libero ut
			quisquam unde quibusdam perspiciatis, repellendus amet accusamus consectetur. Excepturi dolore
			non, officia et expedita aspernatur. Laborum, aperiam odit. Iure molestias modi odit fugit,
			ratione voluptatem eaque corporis reprehenderit ducimus illum est similique. Dolorum sit aut
			amet exercitationem placeat aspernatur quae illo accusamus saepe sunt libero blanditiis ad
			rem, delectus maiores, deleniti necessitatibus commodi quasi? Lorem ipsum dolor sit amet
			consectetur adipisicing elit. Officia voluptatem distinctio tempora molestiae! Maiores eaque
			perspiciatis libero voluptas quod quidem laborum commodi ratione? Repellat atque, architecto
			vero assumenda, totam aliquam saepe enim, ducimus facere dolores laboriosam consequatur magni!
			Explicabo veniam culpa repudiandae, perspiciatis nobis distinctio voluptatem eum reprehenderit
			repellendus incidunt ad facere autem accusamus excepturi impedit sapiente eveniet libero optio
			tenetur esse quis. Ducimus ipsa quia enim ex culpa, in eum illum ea suscipit deserunt placeat
			quos incidunt sed totam neque ab reprehenderit quo libero modi? Vitae eum impedit
			exercitationem, debitis pariatur voluptas aliquid consequuntur dolor, sapiente cumque quod
			quidem, sequi est et libero. Iusto, ipsum delectus atque quidem a quis quibusdam similique
			perspiciatis quaerat inventore tempora sapiente unde nemo animi? Quam ab quibusdam molestias
			odio quo, fugit error eius consequuntur dolor beatae dolore aliquam praesentium culpa?
			Adipisci incidunt ipsa eum reiciendis nihil maiores facilis voluptates hic, soluta magni
			labore necessitatibus maxime neque qui natus dolorem impedit velit earum beatae pariatur
			recusandae, aliquam tempore optio? Aspernatur, fuga unde vitae nam sint a, quam soluta autem
			iste ea illum voluptatem. Ad, repudiandae ea. Enim labore quas odio totam porro, possimus
			aperiam repudiandae nostrum recusandae placeat ratione sequi tenetur dolore cupiditate tempora
			dolor vero iusto, laudantium libero eius optio eos laborum. Officiis commodi minus ipsum
			placeat odio, debitis vitae a cum quasi doloremque eaque provident ex. Tenetur dolorum quo
			fuga, sed ab hic dicta reiciendis ipsa modi aspernatur doloremque enim nam eveniet, aliquid
			aperiam expedita voluptas laborum eaque adipisci. Beatae qui porro blanditiis architecto
			aspernatur maxime culpa quisquam, nam itaque officiis quia accusamus quas ipsa nesciunt
			corporis eius voluptatibus. Quis eos iure maxime illum, aut temporibus reiciendis facere magni
			hic suscipit cum, provident, similique ducimus minima deleniti eligendi expedita? Nobis vel
			facere provident optio neque tenetur, saepe et praesentium modi, culpa mollitia, eligendi quas
			laudantium atque dolores impedit sapiente quo nulla cum nihil aperiam placeat. Earum in amet
			doloribus nostrum architecto quae natus recusandae excepturi! Nemo dolorum, dolor ullam minima
			mollitia odit voluptatem commodi temporibus facilis et repudiandae quas nulla molestiae eaque
			obcaecati amet consectetur! Architecto esse quaerat neque. Corrupti asperiores architecto
			nihil tenetur obcaecati doloribus illum itaque voluptatibus laborum enim reiciendis cupiditate
			id, dolorum quibusdam similique, facere possimus aliquid facilis pariatur? Eius nemo sunt
			expedita omnis magnam, sed voluptatibus impedit aliquid molestias illum nihil totam id
			mollitia hic possimus necessitatibus saepe velit eos consequuntur repellat error! Quia dolores
			beatae possimus asperiores? Obcaecati, nisi. Veritatis autem reiciendis dolorum commodi
			voluptates officia, laudantium molestiae iure maxime fuga labore dolorem excepturi culpa nemo
			enim libero animi cum odio voluptatibus tempore. Aperiam dignissimos laudantium ad placeat
			vitae esse, adipisci libero! Illum magni modi dicta dignissimos sed voluptatem voluptatum
			provident libero ut quisquam unde quibusdam perspiciatis, repellendus amet accusamus
			consectetur. Excepturi dolore non, officia et expedita aspernatur. Laborum, aperiam odit. Iure
			molestias modi odit fugit, ratione voluptatem eaque corporis reprehenderit ducimus illum est
			similique. Dolorum sit aut amet exercitationem placeat aspernatur quae illo accusamus saepe
			sunt libero blanditiis ad rem, delectus maiores, deleniti necessitatibus commodi quasi?
	`;
	let codeEditorBody = `
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia voluptatem distinctio tempora
			molestiae! Maiores eaque perspiciatis libero voluptas quod quidem laborum commodi ratione?
			Repellat atque, architecto vero assumenda, totam aliquam saepe enim, ducimus facere dolores
			laboriosam consequatur magni! Explicabo veniam culpa repudiandae, perspiciatis nobis
			distinctio voluptatem eum reprehenderit repellendus incidunt ad facere autem accusamus
			excepturi impedit sapiente eveniet libero optio tenetur esse quis. Ducimus ipsa quia enim ex
			culpa, in eum illum ea suscipit deserunt placeat quos incidunt sed totam neque ab
			reprehenderit quo libero modi? Vitae eum impedit exercitationem, debitis pariatur voluptas
			aliquid consequuntur dolor, sapiente cumque quod quidem, sequi est et libero. Iusto, ipsum
			delectus atque quidem a quis quibusdam similique perspiciatis quaerat inventore tempora
			sapiente unde nemo animi? Quam ab quibusdam molestias odio quo, fugit error eius consequuntur
			dolor beatae dolore aliquam praesentium culpa? Adipisci incidunt ipsa eum reiciendis nihil
			maiores facilis voluptates hic, soluta magni labore necessitatibus maxime neque qui natus
			dolorem impedit velit earum beatae pariatur recusandae, aliquam tempore optio? Aspernatur,
			fuga unde vitae nam sint a, quam soluta autem iste ea illum voluptatem. Ad, repudiandae ea.
			Enim labore quas odio totam porro, possimus aperiam repudiandae nostrum recusandae placeat
			ratione sequi tenetur dolore cupiditate tempora dolor vero iusto, laudantium libero eius optio
			eos laborum. Officiis commodi minus ipsum placeat odio, debitis vitae a cum quasi doloremque
			eaque provident ex. Tenetur dolorum quo fuga, sed ab hic dicta reiciendis ipsa modi aspernatur
			doloremque enim nam eveniet, aliquid aperiam expedita voluptas laborum eaque adipisci. Beatae
			qui porro blanditiis architecto aspernatur maxime culpa quisquam, nam itaque officiis quia
			accusamus quas ipsa nesciunt corporis eius voluptatibus. Quis eos iure maxime illum, aut
			temporibus reiciendis facere magni hic suscipit cum, provident, similique ducimus minima
			deleniti eligendi expedita? Nobis vel facere provident optio neque tenetur, saepe et
			praesentium modi, culpa mollitia, eligendi quas laudantium atque dolores impedit sapiente quo
			nulla cum nihil aperiam placeat. Earum in amet doloribus nostrum architecto quae natus
			recusandae excepturi! Nemo dolorum, dolor ullam minima mollitia odit voluptatem commodi
			temporibus facilis et repudiandae quas nulla molestiae eaque obcaecati amet consectetur!
			Architecto esse quaerat neque. Corrupti asperiores architecto nihil tenetur obcaecati
			doloribus illum itaque voluptatibus laborum enim reiciendis cupiditate id, dolorum quibusdam
			similique, facere possimus aliquid facilis pariatur? Eius nemo sunt expedita omnis magnam, sed
			voluptatibus impedit aliquid molestias illum nihil totam id mollitia hic possimus
			necessitatibus saepe velit eos consequuntur repellat error! Quia dolores beatae possimus
			asperiores? Obcaecati, nisi. Veritatis autem reiciendis dolorum commodi voluptates officia,
			laudantium molestiae iure maxime fuga labore dolorem excepturi culpa nemo enim libero animi
			cum odio voluptatibus tempore. Aperiam dignissimos laudantium ad placeat vitae esse, adipisci
			libero! Illum magni modi dicta dignissimos sed voluptatem voluptatum provident libero ut
			quisquam unde quibusdam perspiciatis, repellendus amet accusamus consectetur. Excepturi dolore
			non, officia et expedita aspernatur. Laborum, aperiam odit. Iure molestias modi odit fugit,
			ratione voluptatem eaque corporis reprehenderit ducimus illum est similique. Dolorum sit aut
			amet exercitationem placeat aspernatur quae illo accusamus saepe sunt libero blanditiis ad
			rem, delectus maiores, deleniti necessitatibus commodi quasi? Lorem ipsum dolor sit amet
			consectetur adipisicing elit. Officia voluptatem distinctio tempora molestiae! Maiores eaque
			perspiciatis libero voluptas quod quidem laborum commodi ratione? Repellat atque, architecto
			vero assumenda, totam aliquam saepe enim, ducimus facere dolores laboriosam consequatur magni!
			Explicabo veniam culpa repudiandae, perspiciatis nobis distinctio voluptatem eum reprehenderit
			repellendus incidunt ad facere autem accusamus excepturi impedit sapiente eveniet libero optio
			tenetur esse quis. Ducimus ipsa quia enim ex culpa, in eum illum ea suscipit deserunt placeat
			quos incidunt sed totam neque ab reprehenderit quo libero modi? Vitae eum impedit
			exercitationem, debitis pariatur voluptas aliquid consequuntur dolor, sapiente cumque quod
			quidem, sequi est et libero. Iusto, ipsum delectus atque quidem a quis quibusdam similique
			perspiciatis quaerat inventore tempora sapiente unde nemo animi? Quam ab quibusdam molestias
			odio quo, fugit error eius consequuntur dolor beatae dolore aliquam praesentium culpa?
			Adipisci incidunt ipsa eum reiciendis nihil maiores facilis voluptates hic, soluta magni
			labore necessitatibus maxime neque qui natus dolorem impedit velit earum beatae pariatur
			recusandae, aliquam tempore optio? Aspernatur, fuga unde vitae nam sint a, quam soluta autem
			iste ea illum voluptatem. Ad, repudiandae ea. Enim labore quas odio totam porro, possimus
			aperiam repudiandae nostrum recusandae placeat ratione sequi tenetur dolore cupiditate tempora
			dolor vero iusto, laudantium libero eius optio eos laborum. Officiis commodi minus ipsum
			placeat odio, debitis vitae a cum quasi doloremque eaque provident ex. Tenetur dolorum quo
			fuga, sed ab hic dicta reiciendis ipsa modi aspernatur doloremque enim nam eveniet, aliquid
			aperiam expedita voluptas laborum eaque adipisci. Beatae qui porro blanditiis architecto
			aspernatur maxime culpa quisquam, nam itaque officiis quia accusamus quas ipsa nesciunt
			corporis eius voluptatibus. Quis eos iure maxime illum, aut temporibus reiciendis facere magni
			hic suscipit cum, provident, similique ducimus minima deleniti eligendi expedita? Nobis vel
			facere provident optio neque tenetur, saepe et praesentium modi, culpa mollitia, eligendi quas
			laudantium atque dolores impedit sapiente quo nulla cum nihil aperiam placeat. Earum in amet
			doloribus nostrum architecto quae natus recusandae excepturi! Nemo dolorum, dolor ullam minima
			mollitia odit voluptatem commodi temporibus facilis et repudiandae quas nulla molestiae eaque
			obcaecati amet consectetur! Architecto esse quaerat neque. Corrupti asperiores architecto
			nihil tenetur obcaecati doloribus illum itaque voluptatibus laborum enim reiciendis cupiditate
			id, dolorum quibusdam similique, facere possimus aliquid facilis pariatur? Eius nemo sunt
			expedita omnis magnam, sed voluptatibus impedit aliquid molestias illum nihil totam id
			mollitia hic possimus necessitatibus saepe velit eos consequuntur repellat error! Quia dolores
			beatae possimus asperiores? Obcaecati, nisi. Veritatis autem reiciendis dolorum commodi
			voluptates officia, laudantium molestiae iure maxime fuga labore dolorem excepturi culpa nemo
			enim libero animi cum odio voluptatibus tempore. Aperiam dignissimos laudantium ad placeat
			vitae esse, adipisci libero! Illum magni modi dicta dignissimos sed voluptatem voluptatum
			provident libero ut quisquam unde quibusdam perspiciatis, repellendus amet accusamus
			consectetur. Excepturi dolore non, officia et expedita aspernatur. Laborum, aperiam odit. Iure
			molestias modi odit fugit, ratione voluptatem eaque corporis reprehenderit ducimus illum est
			similique. Dolorum sit aut amet exercitationem placeat aspernatur quae illo accusamus saepe
			sunt libero blanditiis ad rem, delectus maiores, deleniti necessitatibus commodi quasi?
	`;
	let outputBody = `
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia voluptatem distinctio tempora
			molestiae! Maiores eaque perspiciatis libero voluptas quod quidem laborum commodi ratione?
			Repellat atque, architecto vero assumenda, totam aliquam saepe enim, ducimus facere dolores
			laboriosam consequatur magni! Explicabo veniam culpa repudiandae, perspiciatis nobis
			distinctio voluptatem eum reprehenderit repellendus incidunt ad facere autem accusamus
			excepturi impedit sapiente eveniet libero optio tenetur esse quis. Ducimus ipsa quia enim ex
			culpa, in eum illum ea suscipit deserunt placeat quos incidunt sed totam neque ab
			reprehenderit quo libero modi? Vitae eum impedit exercitationem, debitis pariatur voluptas
			aliquid consequuntur dolor, sapiente cumque quod quidem, sequi est et libero. Iusto, ipsum
			delectus atque quidem a quis quibusdam similique perspiciatis quaerat inventore tempora
			sapiente unde nemo animi? Quam ab quibusdam molestias odio quo, fugit error eius consequuntur
			dolor beatae dolore aliquam praesentium culpa? Adipisci incidunt ipsa eum reiciendis nihil
			maiores facilis voluptates hic, soluta magni labore necessitatibus maxime neque qui natus
			dolorem impedit velit earum beatae pariatur recusandae, aliquam tempore optio? Aspernatur,
			fuga unde vitae nam sint a, quam soluta autem iste ea illum voluptatem. Ad, repudiandae ea.
			Enim labore quas odio totam porro, possimus aperiam repudiandae nostrum recusandae placeat
			ratione sequi tenetur dolore cupiditate tempora dolor vero iusto, laudantium libero eius optio
			eos laborum. Officiis commodi minus ipsum placeat odio, debitis vitae a cum quasi doloremque
			eaque provident ex. Tenetur dolorum quo fuga, sed ab hic dicta reiciendis ipsa modi aspernatur
			doloremque enim nam eveniet, aliquid aperiam expedita voluptas laborum eaque adipisci. Beatae
			qui porro blanditiis architecto aspernatur maxime culpa quisquam, nam itaque officiis quia
			accusamus quas ipsa nesciunt corporis eius voluptatibus. Quis eos iure maxime illum, aut
			temporibus reiciendis facere magni hic suscipit cum, provident, similique ducimus minima
			deleniti eligendi expedita? Nobis vel facere provident optio neque tenetur, saepe et
			praesentium modi, culpa mollitia, eligendi quas laudantium atque dolores impedit sapiente quo
			nulla cum nihil aperiam placeat. Earum in amet doloribus nostrum architecto quae natus
			recusandae excepturi! Nemo dolorum, dolor ullam minima mollitia odit voluptatem commodi
			temporibus facilis et repudiandae quas nulla molestiae eaque obcaecati amet consectetur!
			Architecto esse quaerat neque. Corrupti asperiores architecto nihil tenetur obcaecati
			doloribus illum itaque voluptatibus laborum enim reiciendis cupiditate id, dolorum quibusdam
			similique, facere possimus aliquid facilis pariatur? Eius nemo sunt expedita omnis magnam, sed
			voluptatibus impedit aliquid molestias illum nihil totam id mollitia hic possimus
			necessitatibus saepe velit eos consequuntur repellat error! Quia dolores beatae possimus
			asperiores? Obcaecati, nisi. Veritatis autem reiciendis dolorum commodi voluptates officia,
			laudantium molestiae iure maxime fuga labore dolorem excepturi culpa nemo enim libero animi
			cum odio voluptatibus tempore. Aperiam dignissimos laudantium ad placeat vitae esse, adipisci
			libero! Illum magni modi dicta dignissimos sed voluptatem voluptatum provident libero ut
			quisquam unde quibusdam perspiciatis, repellendus amet accusamus consectetur. Excepturi dolore
			non, officia et expedita aspernatur. Laborum, aperiam odit. Iure molestias modi odit fugit,
			ratione voluptatem eaque corporis reprehenderit ducimus illum est similique. Dolorum sit aut
			amet exercitationem placeat aspernatur quae illo accusamus saepe sunt libero blanditiis ad
			rem, delectus maiores, deleniti necessitatibus commodi quasi?
	`;
	let pythonStarter = `def main():
	pass`;
	let javaStarter = `class Main {
	public void solution() {

	}
}`;
	let cppStarter = `int main() {
	return 0;
}`;
	let selectedLanguage = 'python';
	/**
	 * @param {Event} event
	 */
	function handleLanguageChange(event) {
		// @ts-ignore
		selectedLanguage = event?.target?.value;
		console.log(selectedLanguage);
	}
</script>

<svelte:head>
	<title>Debug</title>
	<meta name="description" content="The problem to debug" />
</svelte:head>

{#if false}
	<div
		style="position: absolute; left: 50%; top: 30%"
		use:confetti={{
			particleCount: $reduced_motion ? 0 : undefined,
			force: 0.7,
			stageWidth: window.innerWidth,
			stageHeight: window.innerHeight,
			colors: ['#ff3e00', '#40b3ff', '#676778']
		}}
	/>
{/if}

<main>
	<div id="question" class="container">
		<div class="tab-bar">
			<div class="title">Question</div>
			<div class="language-dropdown">
				<select bind:value={selectedLanguage} on:change={handleLanguageChange}>
					<option value="python">Python</option>
					<option value="java">Java</option>
					<option value="cpp">C++</option>
				</select>
			</div>
		</div>
		<div class="body">{questionBody}</div>
	</div>
	<div id="code-editor" class="container">
		<div class="tab-bar">
			<div class="title">Code Editor</div>
			<div class="language-dropdown">
				<select bind:value={selectedLanguage} on:change={handleLanguageChange}>
					<option value="python">Python</option>
					<option value="java">Java</option>
					<option value="cpp">C++</option>
				</select>
			</div>
			<button id="run-code">Run</button>
		</div>
		<div class="body">
			{#if selectedLanguage === 'python'}
				<CustomCodeMirror value={pythonStarter} lang={python} theme={dracula} />
			{:else if selectedLanguage === 'java'}
				<CustomCodeMirror value={javaStarter} lang={java} theme={dracula} />
			{:else if selectedLanguage === 'cpp'}
				<CustomCodeMirror value={cppStarter} lang={cpp} theme={dracula} />
			{:else}
				<CustomCodeMirror value={pythonStarter} lang={python} theme={dracula} />
			{/if}
		</div>
	</div>
	<div id="output" class="container">
		<div class="tab-bar">
			<div class="title">Output</div>
		</div>
		<div class="body">{outputBody}</div>
	</div>
</main>

<style>
	main {
		padding: 1rem;
		display: grid;
		grid:
			'question code-editor'
			'question code-editor'
			'question code-editor'
			'question output';
	}
	#question {
		grid-area: question;
	}
	#code-editor {
		grid-area: code-editor;
	}
	#output {
		grid-area: output;
	}
	.container {
		border: 2px solid #ccc;
		border-radius: 15px;
		background-color: #292929;
		color: white;
		overflow: scroll;
		width: calc(50vw - 2.25rem);
	}
	.container#question {
		width: calc(50vw - 2.25rem);
		height: calc(100vh - 7rem);
	}
	.container#code-editor {
		height: calc((100vh - 7rem) * 0.66);
	}
	.container#output {
		height: calc((100vh - 7rem) * 0.33);
	}
	.tab-bar {
		position: sticky;
		top: 0;
		padding: 0.5rem;
		display: flex;
		font-size: 1.5rem;
		background-color: #333;
		border-radius: 15px 15px 0 0;
	}
	.body {
		padding: 1rem;
	}
	#run-code {
		font-size: 1.25rem;
		background-color: green;
		color: white;
		border: 1px solid whitesmoke;
		border-radius: 5px;
		cursor: pointer;
		transition: all 0.1s ease;
	}
	#run-code:hover {
		background-color: darkgreen;
	}
	#run-code:active {
		background-color: lightgreen;
		color: black;
	}
	#run-code:focus {
		outline: none;
	}

	#code-editor > .tab-bar {
		gap: 1rem;
		display: flex;
	}
	.tab-bar > .title {
		flex: 1;
	}
	.tab-bar > .language-dropdown {
		font-size: 1.25rem;
	}
</style>
