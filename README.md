# MateKids

Aplicació educativa de matemàtiques per a nens, dissenyada per funcionar com a **PWA offline** en iPad (iOS 12.5.8+) i qualsevol navegador modern.

## Funcionalitats

- **Sumes, restes, multiplicacions i divisions** amb 4 nivells de dificultat
- **Divisions pas a pas** en format educatiu europeu (dividend | divisor, quocient sota el divisor)
- Dos modes de pràctica: escriure el resultat o triar entre opcions
- Sistema de recompenses: estrelles, medalles i camí d'aventura
- Missatges motivacionals en català
- Progrés persistent amb `localStorage`
- Teclat numèric integrat (ideal per a tauletes)

## Format de divisió

L'aplicació utilitza el format europeu/espanyol de divisió llarga, tal com s'ensenya a les escoles:

```
  158 | 3
  -15 | ───
  ─── | 52
   08 |
   -6 |
  ─── |
    2 |
```

El nen omple cada pas interactivament: quocient, multiplicació, resta i baixar la xifra.

## PWA / Offline

L'app funciona completament offline gràcies a un Service Worker que guarda tots els recursos en cache.

### Instal·lació a l'iPad (iOS 12.5.8)

1. Obre l'app amb Safari
2. Toca el botó de compartir (quadrat amb fletxa)
3. Selecciona **"Afegir a la pantalla d'inici"**
4. L'app apareixerà com una icona al teu iPad i funcionarà sense connexió

### Servir localment

L'app és un sol fitxer HTML sense dependències. Qualsevol servidor estàtic serveix:

```bash
# Amb Python
python3 -m http.server 8080

# Amb Node.js
npx serve .
```

Obre `http://localhost:8080` al navegador.

## Estructura del projecte

```
mathkids/
├── index.html      # Aplicació completa (HTML + CSS + JS)
├── manifest.json   # Manifest PWA
├── sw.js           # Service Worker per cache offline
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

## Tecnologies

- HTML5, CSS3 (variables, grid, flexbox), JavaScript ES5
- Canvas API per al camí d'aventura
- Service Worker + Cache API per al mode offline
- Zero dependències externes

## Compatibilitat

- iPad amb iOS 12.5.8 (Safari)
- Qualsevol navegador modern (Chrome, Firefox, Edge, Safari)
- Responsive: mòbil, tauleta i escriptori
