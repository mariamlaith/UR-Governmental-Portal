<template>
	<section
		:class="[
			'flex min-h-[calc(100vh-10rem)] items-center justify-center px-5 py-12 transition-colors duration-200 sm:px-8',
			isDarkMode ? 'bg-stone-950 text-stone-100' : 'bg-[#faf7f2] text-[#33231d]'
		]"
		:dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
	>
		<div
			:class="[
				'w-full max-w-md rounded-2xl border p-6 shadow-xl sm:p-8',
				isDarkMode ? 'border-stone-800 bg-stone-900' : 'border-[#e8ddd3] bg-white'
			]"
		>
			<div class="mb-8 text-center">
				<h1 class="text-2xl font-bold sm:text-3xl">
					{{ currentLang === 'ar' ? 'تسجيل الدخول' : 'Sign in' }}
				</h1>
				<p :class="['mt-2 text-sm', isDarkMode ? 'text-stone-400' : 'text-[#6f625a]']">
					{{ currentLang === 'ar' ? 'أدخل بياناتك للمتابعة' : 'Enter your details to continue' }}
				</p>
			</div>

			<form class="space-y-5" @submit.prevent="submitLogin">
				<div>
					<label for="phone" class="mb-2 block text-sm font-bold">
						{{ currentLang === 'ar' ? 'رقم الهاتف' : 'Phone number' }}
					</label>
					<input
						id="phone"
						v-model="phone"
						type="tel"
						inputmode="tel"
						autocomplete="tel"
						required
						:placeholder="currentLang === 'ar' ? 'أدخل رقم الهاتف' : 'Enter your phone number'"
						:class="[
							'w-full rounded-lg border px-4 py-3 text-sm outline-none transition focus:ring-2 focus:ring-[#702923]/30',
							isDarkMode
								? 'border-stone-700 bg-stone-950 text-stone-100 placeholder:text-stone-500'
								: 'border-[#d9ccc2] bg-[#fffdfa] text-[#33231d] placeholder:text-[#9b8d83]'
						]"
					/>
				</div>

				<div>
					<label for="verification-code" class="mb-2 block text-sm font-bold">
						{{ currentLang === 'ar' ? 'رمز التحقق' : 'Verification code' }}
					</label>
					<input
						id="verification-code"
						v-model="verificationCode"
						type="text"
						inputmode="numeric"
						autocomplete="one-time-code"
						required
						maxlength="6"
						:placeholder="currentLang === 'ar' ? 'أدخل رمز التحقق' : 'Enter the verification code'"
						:class="[
							'w-full rounded-lg border px-4 py-3 text-sm outline-none transition focus:ring-2 focus:ring-[#702923]/30',
							isDarkMode
								? 'border-stone-700 bg-stone-950 text-stone-100 placeholder:text-stone-500'
								: 'border-[#d9ccc2] bg-[#fffdfa] text-[#33231d] placeholder:text-[#9b8d83]'
						]"
					/>
				</div>

				<button
					type="submit"
					class="w-full rounded-lg bg-[#702923] px-5 py-3 text-sm font-bold text-white transition-colors hover:bg-[#57201c] focus:outline-none focus:ring-2 focus:ring-[#702923]/40 focus:ring-offset-2"
				>
					{{ currentLang === 'ar' ? 'تسجيل الدخول' : 'Sign in' }}
				</button>
			</form>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Login',
	props: {
		isDarkMode: {
			type: Boolean,
			default: false
		},
		currentLang: {
			type: String,
			default: 'ar'
		}
	},
	data() {
		return {
			phone: '',
			verificationCode: ''
		}
	},
	methods: {
		submitLogin() {
			// Authentication can be connected here once the API is available.
		}
	}
}
</script>
