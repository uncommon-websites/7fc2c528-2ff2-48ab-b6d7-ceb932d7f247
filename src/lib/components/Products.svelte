<script>
  // No script needed
</script>

<div class="space-y-32 pb-32">
  <!-- Energy Router Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Energy Router</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Zero-engineering deployment.</strong> Plug-and-play hardware that activates gigawatts of controllable load instantly. Install in seconds, not months. No rare engineering talent required.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View specs</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Router Visualization -->
      <div class="relative w-full max-w-md">
        <div class="flex justify-between items-center">
          <!-- Central Router -->
          <div class="w-16 h-16 bg-black rounded-lg flex items-center justify-center relative z-10">
            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
              <rect x="2" y="7" width="20" height="10" rx="2"/>
              <circle cx="7" cy="12" r="1" fill="white"/>
              <circle cx="12" cy="12" r="1" fill="white"/>
              <circle cx="17" cy="12" r="1" fill="white"/>
            </svg>
          </div>
          
          <!-- Connected Devices -->
          <div class="flex flex-col gap-3">
            {#each ['HVAC', 'Water Heater', 'EV Charger', 'Pool Pump', 'Battery', 'Solar', 'Thermostat'] as item, i}
              <div class="flex items-center gap-4">
                <div class="w-24 h-[1px] bg-gradient-to-r from-primary-500/30 to-transparent transform rotate-180 origin-left"></div>
                <div class="flex items-center gap-2">
                  <div class="w-3 h-3 rounded-full bg-primary-500"></div>
                  <span class="text-xs font-medium text-gray-600">{item}</span>
                </div>
              </div>
            {/each}
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Platform API Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Platform API</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Real-time grid control.</strong> Simple REST APIs to orchestrate demand response events, monitor device status, and optimize load across thousands of endpoints. Built for scale from day one.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">API documentation</a>
      </div>
    </div>
    <div class="bg-gradient-to-br from-primary-50 to-primary-100 rounded-3xl overflow-hidden min-h-[400px] relative">
      <div class="absolute inset-0 p-8 font-mono text-xs leading-none text-primary-600 opacity-50 break-all overflow-hidden select-none">
        {Array(2000).fill(0).map(() => Math.random().toString(36).substring(2, 3)).join('')}
      </div>
      <div class="absolute inset-0 bg-gradient-to-b from-transparent to-primary-100"></div>
    </div>
  </section>

  <!-- Analytics Dashboard Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Analytics Dashboard</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Real-time insights.</strong> Monitor load profiles, track demand response performance, and optimize grid services revenue. See exactly how your controllable load portfolio performs across all programs.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View demo</a>
      </div>
    </div>
    <div class="bg-black rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Dashboard Mockup -->
      <div class="relative w-64 h-[500px] bg-gray-900 rounded-[3rem] border-8 border-gray-800 shadow-2xl overflow-hidden">
        <!-- Screen Content -->
        <div class="absolute inset-0 bg-black p-4 text-white">
          <div class="flex justify-between items-center mb-6 pt-2">
            <span class="text-xs font-medium">Grid Dashboard</span>
            <div class="w-6 h-6 rounded-full bg-primary-500"></div>
          </div>
          <div class="mb-8">
            <div class="text-2xl font-bold">2.4 GW</div>
            <div class="text-xs text-primary-400">Active capacity</div>
          </div>
          <div class="space-y-3">
             <div class="bg-gray-800/50 p-3 rounded-xl flex items-center gap-3">
               <div class="w-8 h-8 rounded-full bg-primary-500 flex items-center justify-center">
                 <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                   <path d="M13 2L3 14h8l-1 8 10-12h-8l1-8z"/>
                 </svg>
               </div>
               <div class="flex-1">
                 <div class="text-xs font-medium">DR Events</div>
                 <div class="text-[10px] text-gray-400">142 this month</div>
               </div>
               <div class="text-xs">Active</div>
             </div>
             <div class="bg-gray-800/50 p-3 rounded-xl flex items-center gap-3">
               <div class="w-8 h-8 rounded-full bg-green-500 flex items-center justify-center">
                 <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                   <rect x="3" y="3" width="18" height="18" rx="2"/>
                 </svg>
               </div>
               <div class="flex-1">
                 <div class="text-xs font-medium">Devices</div>
                 <div class="text-[10px] text-gray-400">10,247 online</div>
               </div>
               <div class="text-xs">99.8%</div>
             </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>
