<script lang="ts">
	import { enhance } from '$app/forms';
	import { goto } from '$app/navigation';
	import { isLogin } from '../../store';

	let alignment: string = 'code';
</script>

<h3 class="text-center mt-2 mb-10">登录</h3>
<div class="text-center" />

<div class="px-5">
	<label for="phone">手机号</label>
	<input type="text" name="phone" id="phone" class="input" />
	{#if alignment === 'code'}
		<label for="code">验证码</label>
		<div class="flex gap-2">
			<input type="text" placeholder="请输入验证码" class="input" />
			<button class="btn variant-soft-primary">获取验证码</button>
		</div>
	{:else if alignment === 'psw'}
		<label for="password">密码</label>
		<input type="password" name="password" id="password" class="input-group" />
	{/if}
	<button
		class="btn variant-filled-primary w-full my-5"
		on:click={() => {
			setTimeout(() => {
				isLogin.set(true);
				goto('/my');
			}, 500);
		}}>登录</button
	>
	<a class="unstyled" href="/forgetPsw">忘记密码</a>
</div>
