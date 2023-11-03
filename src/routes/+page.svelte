<script>
	const charMap = {
		A: 'Ɐ',
		B: 'ᗺ',
		C: 'Ɔ',
		D: 'ᗡ',
		E: 'Ǝ',
		F: 'Ⅎ',
		G: '⅁',
		H: 'H',
		I: 'I',
		J: 'ᒋ',
		K: 'ꓘ',
		L: '⅂',
		M: 'ꟽ',
		N: 'N',
		O: 'O',
		P: 'Ԁ',
		Q: 'ტ',
		R: 'ᴚ',
		S: 'S',
		T: 'Ʇ',
		U: 'Ո',
		V: 'Λ',
		W: 'M',
		X: 'X',
		Y: '⅄',
		Z: 'Z',
		a: 'ɐ',
		b: 'q',
		c: 'ɔ',
		d: 'p',
		e: 'ǝ',
		f: 'ɟ',
		g: 'ƃ',
		h: 'ɥ',
		i: 'ᴉ',
		j: 'ɾ',
		k: 'ʞ',
		l: 'l',
		m: 'ɯ',
		n: 'u',
		o: 'o',
		p: 'd',
		q: 'b',
		r: 'ɹ',
		s: 's',
		t: 'ʇ',
		u: 'n',
		v: 'ʌ',
		w: 'ʍ',
		x: 'x',
		y: 'ʎ',
		z: 'z',
		'1': '⇂',
		'2': 'ᘔ',
		'3': 'Ɛ',
		'4': '߈',
		'5': 'ဌ',
		'6': '9',
		'7': 'ㄥ',
		'8': '8',
		'9': '6',
		'0': '0'
	};

	let friendName = '';
</script>

<div class="flipper">
	<h1>The friend flipper!</h1>

	<div class="field">
		<label for="friend-name">What's your friend name?</label>
		<input type="text" name="friend-name" placeholder="Vader" bind:value={friendName} />
	</div>

	<h1>
		{#if friendName}
			(╯°□°)╯︵ {friendName
				.split('')
				.map((char) => charMap[char] || char)
				.reverse()
				.join('')}
		{:else}
			(╯°□°)╯︵ ┻━┻
		{/if}
	</h1>
</div>

<style>
	.flipper {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;
	}

	.field {
		margin-bottom: 1rem;
	}

	label {
		display: block;
		margin-bottom: 0.5rem;
	}

	input {
		display: block;
		padding: 0.5rem;
		font-size: 1rem;
		border: 1px solid #ccc;
		border-radius: 0.25rem;
		text-align: center;
	}
</style>
