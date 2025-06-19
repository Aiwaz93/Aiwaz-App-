# Aiwaz-App-
App Mística del Tarot Abrakadab 232, Árbol de la Vida, Rituales y mas...
// AIWAZ ESOTERIC APP - Lienzo Principal COMPLETO
// Tecnología: React + Tailwind CSS + PWA

// ==== INICIO APP ====
import React from "react";
import { BrowserRouter as Router, Route, Routes } from "react-router-dom";

// ==== PÁGINAS ====
const Home = () => (

<div className="p-8 text-center"> <h2 className="text-3xl mb-4">Bienvenido a la AIWAZ ESOTERIC APP</h2> <p className="text-lg">Explora los misterios del Árbol de la Vida, el Tarot Abrakadab 232 y más.</p> </div> );
const AdamKadmon = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🌟 Adam Kadmon Interactivo</h2> <img src="/assets/adam-kadmon.png" alt="Adam Kadmon" className="mx-auto mb-4" /> <p className="text-center">Haz clic en los puntos energéticos para recibir mensajes esotéricos.</p> </div> );
const Sephiroth = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🌳 Árbol de la Vida</h2> <img src="/assets/sephiroth.png" alt="Árbol de la Vida" className="mx-auto mb-4" /> <p className="text-center">Cada esfera representa una Sephirah y una carta del Tarot.</p> </div> );
const Gematria = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🔤 Letras Hebreas y Gematría</h2> <ul className="list-disc list-inside"> <li>Aleph - 1 - Espíritu - א (Audio)</li> <li>Bet - 2 - Casa - ב (Audio)</li> {/* Continúa con las 22 letras */} </ul> </div> );
const Tarot = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🎴 Tarot Abrakadab 232</h2> <div className="grid grid-cols-2 md:grid-cols-4 gap-4"> <div className="bg-black border border-gold p-2">El Loco - Aleph - Kether</div> <div className="bg-black border border-gold p-2">El Mago - Beth - Yesod</div> </div> </div> );
const Lecturas = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🔮 Lecturas de Tarot Gratuitas</h2> <ul className="list-decimal list-inside mb-4"> <li>1 carta: Arcano Mayor (2 veces)</li> <li>3 cartas: Pasado-Presente-Futuro (2 veces)</li> <li>4 cartas: Fases lunares (2 veces)</li> <li>10 cartas: Sephiroth y senderos (1 vez)</li> </ul> <p className="italic">Para seguir consultando, suscríbete a uno de nuestros planes.</p> </div> );
const Rituales = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">🕯 Rituales y Prácticas</h2> <ul className="list-disc list-inside"> <li>Limpieza energética (Gratuito)</li> <li>Ritual del amor (VIP)</li> <li>Abundancia, éxito, iniciación (VIP)</li> </ul> </div> );
const Biblioteca = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">📚 Biblioteca Virtual 232</h2> <p>Explora fragmentos narrados por voz femenina y descarga libros si eres suscriptor.</p> <ul className="list-disc list-inside mt-4"> <li>Libro del Tarot Abrakadab 232 (descarga VIP)</li> <li>Kybalion (público)</li> </ul> </div> );
const Suscripcion = () => (

<div className="p-8"> <h2 className="text-2xl mb-4">💎 Planes de Suscripción</h2> <ul className="list-disc list-inside"> <li>Luz del Iniciado – $33.3 USD</li> <li>Pilar del Mago – $66.6 USD</li> <li>Corona de Aiwaz – $120 USD</li> </ul> <p className="mt-4 italic">Paga vía PayPal o transferencia. Envíanos un correo para activar tu cuenta VIP.</p> </div> );
const Traduccion = () => (

<div className="flex justify-end p-2"> <select className="bg-black border border-gold text-gold"> <option>Español</option> <option>Inglés</option> <option>Francés</option> <option>Japonés</option> <option>Portugués</option> <option>Italiano</option> <option>Alemán</option> </select> </div> );
function App() {
return (
<Router>
<div className="bg-black text-gold min-h-screen font-serif">
<header className="text-center p-4 border-b border-gold">
<h1 className="text-4xl font-bold tracking-widest">AIWAZ ESOTERIC APP</h1>
<p className="text-sm">Por Frater Abrakadab</p>
</header>
<Traduccion />
<Routes>
<Route path="/" element={<Home />} />
<Route path="/adam-kadmon" element={<AdamKadmon />} />
<Route path="/sephiroth" element={<Sephiroth />} />
<Route path="/gematria" element={<Gematria />} />
<Route path="/tarot" element={<Tarot />} />
<Route path="/biblioteca" element={<Biblioteca />} />
<Route path="/rituales" element={<Rituales />} />
<Route path="/lecturas" element={<Lecturas />} />
<Route path="/suscripcion" element={<Suscripcion />} />
</Routes>
</div>
</Router>
);
}

export default App;

// === tailwind.config.js ===
/** @type {import('tailwindcss').Config} /
module.exports = {
content: ["./src/**/.{js,jsx,ts,tsx}"],
theme: {
extend: {
colors: {
gold: '#FFD700',
cosmic: '#0B0C10'
},
fontFamily: {
serif: ['Cinzel Decorative', 'serif']
}
},
},
plugins: [],
};

// === index.css ===
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
background-color: #0B0C10;
color: #FFD700;
font-family: 'Cinzel Decorative', serif;
}

// === manifest.json ===
{
"short_name": "AIWAZ",
"name": "AIWAZ ESOTERIC APP",
"icons": [
{
"src": "/assets/icon.png",
"type": "image/png",
"sizes": "512x512"
}
],
"start_url": ".",
"display": "standalone",
"theme_color": "#0B0C10",
"background_color": "#000000"
}

// === serviceWorker.js ===
self.addEventListener('install', function(e) {
e.waitUntil(
caches.open('aiwaz-store').then(function(cache) {
return cache.addAll([
'/',
'/index.html',
'/assets/icon.png'
]);
})
);
});

self.addEventListener('fetch', function(e) {
e.respondWith(
caches.match(e.request).then(function(response) {
return response || fetch(e.request);
})
);
});

// === Registro del Service Worker en index.js ===
if ('serviceWorker' in navigator) {
window.addEventListener('load', () => {
navigator.serviceWorker.register('/serviceWorker.js')
.then(reg => console.log('SW registrado', reg))
.catch(err => console.error('SW fallo', err));
});
}
