<script lang="ts">
	function drawerClose(): void {}
</script>

<nav class="list-nav p-4">
	<ul>
		<li><a href="/" on:click={drawerClose}>市场</a></li>
		<li><a href="/about" on:click={drawerClose}>我的</a></li>
		<!-- <li><a href="/blog" on:click={drawerClose}>Blog</a></li>
		<li><a href="/contact" on:click={drawerClose}>Contact</a></li> -->
	</ul>
</nav>
