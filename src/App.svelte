<script>
    import Hello from './Hello.svelte';
    import Groceries from './Groceries.svelte';
    import Shapes from './Shapes.svelte';
    import Buttons from './Buttons.svelte';
    import Text_fields from './Text-fields.svelte';
    import Forms from './Forms.svelte';
    import Numbers from './Numbers.svelte';
    import Cards from './Cards.svelte';
    let example = Hello;
</script>

<main>
	<h1>Elm Examples written in Svelte</h1>
    <div class="box">
        <div class="col1">
            <div class="link" on:click='{() => example=Hello}'>Hello</div>
            <div class="link" on:click='{() => example=Groceries}'>Groceries</div>
            <div class="link" on:click='{() => example=Shapes}'>Shapes</div>
            <div class="link" on:click='{() => example=Buttons}'>Buttons</div>
            <div class="link" on:click='{() => example=Text_fields}'>Text-fields</div>
            <div class="link" on:click='{() => example=Forms}'>Forms</div>
            <div class="link" on:click='{() => example=Numbers}'>Numbers</div>
            <div class="link" on:click='{() => example=Cards}'>Cards</div>
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
