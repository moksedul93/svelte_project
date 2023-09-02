<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<div class="layout">
	<div class="md:flex">
		<div class="w-full h-full md:w-6/12">
			<div class="flex">
				<div class="flex flex-col w-4/12">
						<div class="w-full h-96 bg-blue-400 flex justify-center items-center">
							<div>3 x 2(color:blue-400)</div>
						</div>
						<div class="w-full h-64 bg-teal-400 flex justify-center items-center">
							<div>3 x 2(color:teal-400)</div>
						</div>
				</div>
				<div class="w-8/12 bg-rose-100 flex justify-center items-center">
					<div>5 x 4(color:rose-400)</div>
				</div>
			</div>
			<div class="w-full h-32 bg-fuchsia-400 flex justify-center items-center">
					<div>2 x 2(color:fuchsia-400)</div>
			</div>
		</div>
		<div class="w-full h-full md:w-6/12">
			<div class="w-full h-64 bg-blue-400 flex justify-center items-center">
					<div>2 x 6(color:blue-400)</div>
			</div>
			<div class="flex">
				<div class="w-8/12 h-[32rem] bg-yellow-100 flex flex-col justify-center items-center">
					<div>4 x 4(color:yellow-100)</div>
					<div class="h-[300px] w-[300px] bg-[#293462] flex justify-center items-center">
							<div class="h-[200px] w-[200px] bg-yellow-100 rounded-full relative">
								<div class="c3 w-[120px] h-[120px]"><div class="circ3"></div></div>
								<div class="c4 w-[150px] h-[150px]"><div class="circ4"></div></div>
							</div>
					</div>
				</div>
				<div class="w-4/12 h-[32rem] bg-emerald-400 flex justify-center items-center">
					<div>4 x 2(color:emerald-400)</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
.c3{
	position: absolute;
    border-radius:0;
    background: #12546b;
    transform: rotate(38deg);
    overflow: hidden;
} 
.c4{
	position: absolute;
    border-radius: 0;
    background: #12546b;
    transform: rotate(38deg);
    overflow: hidden;
}
</style>