<svelte:head>
	<title>Chat</title>
	<meta name="description" content="chart this app" />
</svelte:head>
<script>
	import {onMount} from "svelte";
	import {countryDataStore} from "../../store";
	
	onMount(async () => {
		try {
			const response = await fetch("https://restcountries.com/v3.1/all");
			const data = await response.json();
			console.log("Fetched data:", data); // Check if data is fetched
			countryDataStore.set(data);
		} catch (error) {
			console.error("Error fetching data:", error);
		}
	});
</script>


	<div>
		<h1>Chart Page:</h1>
		<div class="flex">
			<div class="chart-table w-9/12">
				{#if $countryDataStore.length > 0}
				<table class="min-w-full table-auto leading-normal">
						<thead>
							<tr>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
									Flag
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
									Name
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
									POPULATION
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-center text-xs font-semibold text-gray-700 uppercase tracking-wider">
									CIOC
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-center text-xs font-semibold text-gray-700 uppercase tracking-wider">
									UN Member Status
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-center text-xs font-semibold text-gray-700 uppercase tracking-wider">
									Currencies
							</th>
								<th
									class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
									Languages
							</th>
							</tr>
						</thead>
							<tbody>
								{#each $countryDataStore as country, index (index)}
									<tr key={index}>
										<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
											<div class="flex">
												<div class="flex-shrink-0 w-10 h-10">
													{#if country.flags.png}
												<img class="w-full h-full rounded-full" src={country.flags.png} alt={country.name.common} />
													{:else}
												<p>Flag not available</p>
													{/if}
											</div>
											</div>
										</td>
										<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm min-w-[170px]">
											<p class="text-gray-900 whitespace-no-wrap">{country.name.common}</p>
										</td>
										<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
											<p class="text-gray-900 whitespace-no-wrap">{country.population}</p>
										</td>
										<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm text-center min-w-[170px]">
											{#if country.cioc}
											<p class="text-gray-900 whitespace-no-wrap">{country.cioc}</p>
											{:else}
											<p class="text-gray-900 whitespace-no-wrap">Not Available</p>
											{/if}
										</td>
											<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm text-center min-w-[170px]">
												<span class="relative inline-block px-3 py-1 font-semibold text-green-900 leading-tight">
													<span aria-hidden class="absolute inset-0 bg-green-200 opacity-50 rounded-lg"></span>
													<span class="relative">{#if country.unMember}
													<p class="text-green-900">Yes</p>
														{:else}
														<p class="text-red-900">No</p>
														{/if}
												</span>
												</span>
											</td>
											<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm text-center">
												{#if country.currencies}
												{#each Object.keys(country.currencies) as currencyCode}
												<p class="text-gray-900 whitespace-no-wrap">
													{currencyCode}
												</p>
												{/each}
											{:else}
																No currency available
											{/if}
										</td>
										<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
											{#if country.languages}
												<p class="text-gray-900 whitespace-no-wrap">
													{Object.values(country.languages).join(', ')}
												</p>
												{:else}
													No languages available
											{/if}
										</td>
									</tr>
								{/each}
						</tbody>
					</table>
					{:else}
						<p>Loading data...</p>
					{/if}
			</div>
			<div class="chart w-3/12">
				ddd
			</div>

		</div>
	</div>