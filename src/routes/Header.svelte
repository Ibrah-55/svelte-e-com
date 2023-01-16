<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/groceryw.png';
	import shopping from '$lib/images/shopping-cart.png';
	import profile from '$lib/images/profile.webp';

</script>

<header>
	<div class="corner1">
		<a href="/">
			<img src={logo} alt="Grocery" />
		</a>
	</div>

	<nav>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">Breakfast Cereals</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
				<a href="/sverdle">Fresh Vegetables</a>
			</li>
		</ul>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Sauses  Spices</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">  </a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
				<a href="/sverdle">Fresh Fruits</a>
			</li>
		</ul><ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Fresh Juice</a>
			</li>
		
			<li aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
				<a href="/sverdle">Vegetable salads</a>
			</li>
		</ul><ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Yoghurt Smoothies</a>
			</li>
			
		
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
		<div class="flex items-center justify-center ">
			<div class="flex border-2 border-gray-200 rounded">
				<input type="text" class="px-4 py-2 w-80" placeholder="Search...">
				<button class="px-4 text-white bg-gray-600 border-l ">
					Search
				</button>
			</div>
		</div>
	</ul>
	</nav>
<div class="corner">
		<a href="/profile" aria-current={$page.url.pathname === '/profile' ? 'page' : undefined}>
			<img src={profile} alt="profile" />
		</a>
	</div>
	<div class="corner">
		<a href="/cart" aria-current={$page.url.pathname === '/cart' ? 'page' : undefined}>
			<img src={shopping} alt="cart" />
		</a>
	</div>
</header>

<style>

	header {
		display: flex;
		justify-content: space-between;

	}
	.corner1 img{
		width: 6em;
		height: 4em;
		object-fit: contain;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 3em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		align-items: left;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
