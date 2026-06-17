// Objeto donde se guarda toda la información de los destinos
const data = {

  // Información sobre Maldivas
  maldives: {
    name: "Maldivas",
    hero: "https://images.unsplash.com/photo-1573843981267-be1999ff37cd",

    // Hotel recomendado para este destino
    hotel: {
      name: "Mar Salada Resort",
      img: "https://images.unsplash.com/photo-1566073771259-6a8506099945",
      desc: "Resort de lujo sobre el mar cristalino."
    },

    // Lista de vuelos disponibles
    flights: [
      { route: "Barcelona → Maldivas", time: "08:30" }
    ],

    // Restaurante recomendado
    restaurant: {
      name: "Blue Lagoon",
      desc: "Comida tropical frente al mar."
    }
  },

  // Información sobre Nueva York
  newyork: {
    name: "New York",
    hero: "https://images.unsplash.com/photo-1499092346589-b9b6be3e94b2",

    // Hotel recomendado
    hotel: {
      name: "Skyline Hotel",
      img: "https://images.unsplash.com/photo-1542314831-068cd1dbfeeb",
      desc: "Hotel moderno en Manhattan."
    },

    // Vuelo disponible
    flights: [
      { route: "Madrid → New York", time: "16:45" }
    ],

    // Restaurante recomendado
    restaurant: {
      name: "Sky Diner",
      desc: "Comida urbana con vistas a la ciudad."
    }
  },

  // Información sobre Florencia
  florence: {
    name: "Florencia",
    hero: "https://content-viajes.nationalgeographic.com.es/medio/2025/09/22/adobestock-119593111_d8651c0d_250922124617_1280x854.webp$0",

    // Hotel recomendado
    hotel: {
      name: "Villa Toscana",
      img: "https://www.rodaonline.com/wp-content/uploads/Roda-Projects-VillaToscana-02.jpg$0",
      desc: "Hotel con encanto italiano."
    },

    // Vuelo disponible
    flights: [
      { route: "Barcelona → Florencia", time: "09:15" }
    ],

    // Restaurante recomendado
    restaurant: {
      name: "Trattoria Roma",
      desc: "Auténtica cocina italiana."
    }
  }
};

// Función que muestra una página concreta
function showPage(pageId) {

  // Seleccionamos todas las páginas de la aplicación
  const pages = document.querySelectorAll(".page");

  // Quitamos la clase "active" de todas las páginas
  pages.forEach(p => p.classList.remove("active"));

  // Seleccionamos la página que queremos mostrar
  const page = document.getElementById(pageId);

  // Añadimos la clase "active" para hacerla visible
  page.classList.add("active");

  // Si existe información para ese destino, la mostramos
  if (data[pageId]) {
    renderDestination(pageId);
  }
}

// Función que crea el contenido de cada destino
function renderDestination(id) {

  // Guardamos los datos del destino seleccionado
  const d = data[id];

  // Variable donde se irán guardando los vuelos en formato HTML
  let flightsHTML = "";

  // Recorremos todos los vuelos disponibles
  d.flights.forEach(f => {

    // Añadimos cada vuelo a la variable flightsHTML
    flightsHTML += `
      <div class="flight-card">
        ${f.route}<br><strong>${f.time}</strong>
      </div>
    `;
  });

  // Insertamos todo el contenido dentro de la página correspondiente
  document.getElementById(id).innerHTML = `

    <!-- Botón para volver a la página principal -->
    <button class="back" onclick="showPage('home')">← Volver</button>

    <!-- Nombre del destino -->
    <h1>${d.name}</h1>

    <!-- Imagen principal del destino -->
    <img class="hero" src="${d.hero}">

    <!-- Sección del hotel recomendado -->
    <h2> Hotel recomendado</h2>

    <div class="hotel-card">
      <img src="${d.hotel.img}">
      <h3>${d.hotel.name}</h3>
      <p>${d.hotel.desc}</p>
    </div>

    <!-- Sección de vuelos -->
    <h2> Vuelos disponibles</h2>

    ${flightsHTML}

    <!-- Sección del restaurante recomendado -->
    <h2> Restaurante recomendado</h2>

    <div class="restaurant-card">
      <h3>${d.restaurant.name}</h3>
      <p>${d.restaurant.desc}</p>
    </div>
  `;
}


