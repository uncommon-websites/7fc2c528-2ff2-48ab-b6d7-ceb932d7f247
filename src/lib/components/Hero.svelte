<script>
  let activeTab = 'Demand Response';
  const tabs = ['Demand Response', 'Load Control', 'Grid Services', 'Peak Shaving', 'Frequency Regulation', 'Virtual Power Plant', 'Energy Trading', 'Capacity Market'];
</script>

<section class="pt-32 pb-20 px-6 max-w-7xl mx-auto">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
    <div>
      <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black leading-[1.1] mb-8">
        Zero-engineering <br /> energy management
      </h1>
    </div>
    <div class="flex flex-col justify-end items-start lg:pl-12">
      <p class="text-xl text-gray-600 mb-6 max-w-md leading-relaxed">
        Deploy gigawatts of controllable load instantly. Transform energy retailers into grid-interactive powerhouses with hardware that installs in seconds.
      </p>
      <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
        Explore Platform 
        <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
      </a>
    </div>
  </div>

  <!-- Interactive Visual Section -->
  <div class="rounded-3xl overflow-hidden bg-gray-50 border border-gray-200 shadow-sm">
    <!-- Tabs -->
    <div class="flex overflow-x-auto scrollbar-hide border-b border-gray-200 bg-white/50 backdrop-blur-sm">
      {#each tabs as tab}
        <button 
          class="px-5 py-4 text-sm font-medium whitespace-nowrap transition-colors relative {activeTab === tab ? 'text-black' : 'text-gray-500 hover:text-gray-800'}"
          on:click={() => activeTab = tab}
        >
          {tab}
          {#if activeTab === tab}
            <div class="absolute bottom-0 left-0 right-0 h-0.5 bg-black"></div>
          {/if}
        </button>
      {/each}
    </div>

    <!-- Content Area -->
    <div class="relative h-[500px] bg-gradient-to-br from-gray-900 to-gray-800 overflow-hidden group">
      <!-- Grid Pattern Background -->
      <div class="absolute inset-0 opacity-20" 
           style="background-image: linear-gradient(rgba(255,255,255,0.1) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.1) 1px, transparent 1px); background-size: 40px 40px;">
      </div>
      
      <!-- Floating UI Card - Energy Dashboard -->
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-4 text-white shadow-2xl">
        <div class="flex justify-between items-center mb-6">
          <span class="text-xs font-medium text-white/80">Live Grid Status</span>
          <div class="px-2 py-1 rounded-full bg-primary-500/20 text-primary-300 text-[10px] font-medium">Active</div>
        </div>
        
        <!-- Load Control Event -->
        <div class="flex items-center gap-3 mb-4">
          <div class="w-10 h-10 rounded-full bg-primary-500 flex items-center justify-center text-white shrink-0">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M13 2L3 14h8l-1 8 10-12h-8l1-8z"/>
            </svg>
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">Peak Event</h3>
              <span class="text-sm font-medium">2.4 GW</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">Active now</p>
              <p class="text-xs text-primary-300">Curtailed</p>
            </div>
          </div>
        </div>

        <!-- Device Status -->
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-white flex items-center justify-center text-gray-900 shrink-0">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <rect x="3" y="3" width="18" height="18" rx="2"/>
              <path d="M9 9h6v6H9z"/>
            </svg>
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">Energy Routers</h3>
              <span class="text-sm font-medium">10,247</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">Connected</p>
              <div class="px-1.5 py-0.5 rounded bg-white/20 text-[10px] font-medium">99.8%</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Code Block -->
    <div class="bg-gray-50 p-6 border-t border-gray-200 overflow-x-auto">
      <pre class="font-mono text-xs leading-relaxed text-gray-600">
<span class="text-gray-400 select-none">1</span>  <span class="text-gray-400"># Deploy demand response event across 10k+ devices in seconds</span>
<span class="text-gray-400 select-none">2</span>
<span class="text-gray-400 select-none">3</span>  <span class="text-purple-600">curl</span> <span class="text-blue-600">-X POST</span> <span class="text-green-600">'https://api.elastic.energy/v1/events'</span> \
<span class="text-gray-400 select-none">4</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Authorization: Bearer &lt;your-api-key&gt;'</span> \
<span class="text-gray-400 select-none">5</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Content-Type: application/json'</span> \
<span class="text-gray-400 select-none">6</span>    <span class="text-blue-600">-d</span> '&#123;
<span class="text-gray-400 select-none">7</span>      <span class="text-blue-800">"event_type"</span>: <span class="text-green-600">"demand_response"</span>,
<span class="text-gray-400 select-none">8</span>      <span class="text-blue-800">"target_load"</span>: <span class="text-green-600">"2.4GW"</span>,
<span class="text-gray-400 select-none">9</span>      <span class="text-blue-800">"duration"</span>: <span class="text-green-600">"4h"</span>,
<span class="text-gray-400 select-none">10</span>     <span class="text-blue-800">"device_groups"</span>: [<span class="text-green-600">"hvac"</span>, <span class="text-green-600">"water_heaters"</span>],
<span class="text-gray-400 select-none">11</span>     <span class="text-blue-800">"priority"</span>: <span class="text-green-600">"high"</span>
<span class="text-gray-400 select-none">12</span>   &#125;'</pre>
    </div>
  </div>
</section>
