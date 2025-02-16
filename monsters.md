---
layout: default
title: Monster Compendium
---

<div class="container mx-auto px-4 py-8 max-w-4xl">
  <h1 class="text-4xl font-bold mb-8">Monster Compendium</h1>
  
  <div class="mb-8">
    <input type="text" 
           id="monsterSearch" 
           placeholder="Search monsters..." 
           class="w-full p-2 border rounded"
           onkeyup="filterMonsters()">
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4" id="monsterGrid">
    {% for monster in site.monsters %}
      <a href="{{ monster.url }}" class="monster-card p-4 border rounded hover:shadow-lg transition-shadow">
        <h2 class="text-xl font-bold">{{ monster.name }}</h2>
        <p class="text-gray-600">{{ monster.type }}, {{ monster.alignment }}</p>
        <p class="text-gray-600">CR {{ monster.challenge_rating.rating }}</p>
      </a>
    {% endfor %}
  </div>
</div>

<script>
function filterMonsters() {
  const input = document.getElementById('monsterSearch');
  const filter = input.value.toLowerCase();
  const cards = document.getElementsByClassName('monster-card');

  for (let card of cards) {
    const text = card.textContent.toLowerCase();
    card.style.display = text.includes(filter) ? '' : 'none';
  }
}
</script>