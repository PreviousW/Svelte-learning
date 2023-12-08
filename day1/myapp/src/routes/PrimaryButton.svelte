<script>
    //@ts-nocheck
    import { createEventDispatcher } from 'svelte';

    export let name;
    export let url;
    const dispatch = createEventDispatcher();

    function cDispatch() {
		dispatch('multiplyclick', {
			uri: url,
            name: name,
		});
	}

        
    </script>
<button on:click={cDispatch} on:keyup>{name}</button>

<style>
    button {
        background-color: #25AEFB;
        border-color: #25AEFB;
        font-style: normal;
        font-size: 1.2em;
        color: #E3F7FD;
        border-radius: 10%;
        width: 150px;
        height: 50px;
    }
</style>
