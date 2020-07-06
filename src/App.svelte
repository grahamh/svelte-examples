<script>
    export let name;
    import Page1 from './Page1.svelte';
    import Page2 from './Page2.svelte';
    let example = Page1;
</script>

<main>
	<h1>Hello {name}!</h1>
    <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
    <div class="box">
        <div class="col1">
            <div class="link" on:click='{() => example=Page1}'>Page 1</div>
            <div class="link" on:click='{() => example=Page2}'>Page 2</div>
        </div>
        <div class="col2">
            <svelte:component this={example}/>
        </div>
    </div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
    }

    .link {
        cursor: pointer;
        text-decoration: underline;
        color: blue;
    }

    .box {
        display: flex;
        text-align: left;
    }

    .col1 {
        flex: 1 1 auto;
    }

    .col2 {
        flex: 3 1 auto;
    }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
