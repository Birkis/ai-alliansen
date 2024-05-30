<script>
    let name = '';
    let email = '';
    let address = '';
    let message = '';

    let items = [
    { text: "Innføre en universell grunninntekt (UBI) for å sikre økonomisk trygghet for alle borgere, finansiert av AI-generert velstand." },
    { text: "Innføre en rettferdig beskatning på AI-generert inntekt for å sikre at velstanden fordeles blant hele befolkningen, ikke bare hos store selskaper." },
    { text: "Implementere strenge etiske og juridiske retningslinjer for utvikling og bruk av AI for å beskytte personvern og sikre ansvarlig innovasjon." },
    { text: "Bygge en nasjonal serverpark og AI-infrastruktur for å sikre at Norge beholder suverenitet og kontroll over vår egen AI-teknologi og data." }
    ];
  
    const requestForm = () => {
      // Here, you would handle the form request, e.g., send the information to your backend
      message = `Takk, ${name}. Vi vil sende skjemaet til ${address}.`;
    };
  </script>
  
  <main class="min-h-screen bg-gray-100 text-gray-900">
    <header class="bg-blue-600 text-white py-4">
      <div class="container mx-auto px-4">
        <h1 class="text-3xl font-bold">AI-alliansen</h1>
        <p class="mt-2">Hjelp oss med å samle 5000 underskrifter for å registrere vårt parti!</p>
      </div>
    </header>
    
    <section class="container mx-auto px-4 py-8">
      <h2 class="text-2xl font-semibold mb-4">Bli med oss</h2>
      <p class="mb-6">Vi jobber for å skape en bedre fremtid. Støtt vår sak ved å signere vårt skjema. Du kan enten laste ned skjemaet eller be oss sende det til deg.</p>
      
      <div class="mb-8">
        <h3 class="text-xl font-semibold mb-2">Last ned skjemaet</h3>
        <a href="https://drive.google.com/file/d/1rknTONjqfXqdd2d5Pi_YUD69aDMLT922/view?usp=sharing" class="bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700">Last ned skjema</a>
      </div>
      
      <div>
        <h3 class="text-xl font-semibold mb-2">Be om et skjema via post</h3>
        <form on:submit|preventDefault={requestForm} class="space-y-4">
          <div>
            <label for="name" class="block font-medium">Fullt navn</label>
            <input type="text" id="name" bind:value={name} class="w-full px-4 py-2 border rounded" required />
          </div>
          <div>
            <label for="email" class="block font-medium">E-post</label>
            <input type="email" id="email" bind:value={email} class="w-full px-4 py-2 border rounded" required />
          </div>
          <div>
            <label for="address" class="block font-medium">Postadresse</label>
            <textarea id="address" bind:value={address} class="w-full px-4 py-2 border rounded" rows="4" required></textarea>
          </div>
          <button type="submit" class="bg-green-600 text-white py-2 px-4 rounded hover:bg-green-700">Be om skjema</button>
        </form>
        {#if message}
          <p class="mt-4 text-green-600">{message}</p>
        {/if}
      </div>
    </section>
    
    <section class="container mx-auto px-4 py-8 bg-white shadow-md rounded">
      <h2 class="text-2xl font-semibold mb-4">AI-alliansens partiprogram</h2>
      <p class="mb-6">AI-alliansen er et norsk politisk parti dedikert til å sikre at menneskeheten er forberedt på AGI-æraen (kunstig generell intelligens). Vårt mål er å sikre at rikdommen generert av AGI kommer hele menneskeheten til gode, ikke bare "eierne" av modellene og forretningstycoonene.</p>
      <h3 class="text-xl font-semibold mb-2">Våre mål</h3>
      <ul class="list-disc list-inside mb-6">
            {#each items as item (item.text)}
                <li class="py-2">{item.text}</li>
        {/each}
    </ul>
      <h3 class="text-xl font-semibold mb-2">Hvorfor bli med i AI-alliansen?</h3>
      <p class="mb-6">Vi ser at dagens politikere ofte har et kortsiktig fokus og mangler teknologisk forståelse for de store endringene som kommer med AI. AI-alliansen vil sikre at Norge er forberedt på AI-æraen ved å tenke langsiktig og teknologisk fremover. Ved å bli med i AI-alliansen blir du en del av en bevegelse som har som mål å forme fremtiden for AI på en måte som gagner alle. Sammen kan vi sørge for at fremskrittene innen AI og AGI leder til et mer rettferdig og velstående samfunn for alle.</p>
    </section>
  </main>
  
  <style>
    .container {
      max-width: 800px;
    }
  </style>
  