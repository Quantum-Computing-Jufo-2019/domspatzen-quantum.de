<template>
	<div class="download">
		<a class="download_a" :href="href" target="_blank" rel="noreferrer">
			<img class="download_icon" alt="Download" src="~/assets/download.svg">
			<p class="download_text">{{ content }}</p>
		</a>
	</div>
</template>
<script>
export default {
	props: {
		content: {
			type: String,
			default: "",
		},
		href: {
			type: String,
			default: "",
		},
	},
};
</script>
<style>
	.download {
		margin: 5px;
		padding: 5px;
		display: flex;
		flex-flow: column;
		justify-content: center;
		background-color: var(--green3);
		border-radius: 7px;
		flex-grow: 200;
		flex-shrink: 0;
	}
	.download_a {
		color: black;
		text-decoration: none;
	}
	.download_icon {
		width: 50px;
		display: block;
		margin-left: auto;
		margin-right: auto;
    -moz-user-select: none;
    -webkit-user-select: none;
    user-select: none;
  }
	.download_text {
		text-align: center;
		font-size: 20px;
		margin: 4px 0 4px 0;
	}
	@media (pointer:none), (pointer:coarse) {
		.download_text {
				font-size: 30px;
				overflow-wrap: break-word;
		}
		.download_icon {
			display: none;
		}
	}
</style>
