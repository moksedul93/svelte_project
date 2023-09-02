<svelte:head>
	<title>Chat</title>
	<meta name="description" content="chart this app" />
</svelte:head>


<div>
	<h1>Chart Page:</h1>
	<div class="flex">
		<div class="chart-table w-9/12">
			<table class="min-w-full leading-normal">
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
							class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
							CIOC
						</th>
						<th
							class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
							UN Member Status
						</th>
						<th
							class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
							Currencies
						</th>
						<th
							class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-700 uppercase tracking-wider">
							Languages
						</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<div class="flex">
								<div class="flex-shrink-0 w-10 h-10">
									<img class="w-full h-full rounded-full"
										src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.2&w=160&h=160&q=80"
										alt="" />
								</div>
							</div>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<p class="text-gray-900 whitespace-no-wrap">name</p>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<p class="text-gray-900 whitespace-no-wrap">2000000</p>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<p class="text-gray-900 whitespace-no-wrap">RSI</p>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<span class="relative inline-block px-3 py-1 font-semibold text-green-900 leading-tight">
								<span aria-hidden class="absolute inset-0 bg-green-200 opacity-50 rounded-lg"></span>
								<span class="relative">Yes</span>
							</span>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<p class="text-gray-900 whitespace-no-wrap">NOC</p>
						</td>
						<td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
							<p class="text-gray-900 whitespace-no-wrap">English</p>
						</td>
					</tr>
				</tbody>
			</table>
		</div>
		<div class="chart w-3/12">
			ddd
		</div>

	</div>
</div>