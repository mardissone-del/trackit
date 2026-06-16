# TrackIt — Landing + demo

Sitio de **TrackIt**, app de finanzas personales para jóvenes en Argentina.
Es la landing/demo del producto (medio propio del plan de marketing).
100% estático: **un solo archivo `index.html`**, sin frameworks ni build. Se hospeda gratis en **GitHub Pages**.

---

## Qué subir al repo

```
trackit/
├── index.html   <- obligatorio (es todo el sitio)
└── README.md    <- opcional, este archivo
```

Solo `index.html` es necesario. No hace falta nada más: las fuentes se cargan desde Google Fonts y el favicon va embebido.

---

## Cómo deployarlo en GitHub Pages

### Opcion A - desde la web (sin instalar nada)
1. Crea un repositorio **publico** en GitHub, por ejemplo `trackit`.
2. **Add file -> Upload files**, arrastra `index.html` (y `README.md`) y hace **Commit changes**.
3. Entra a **Settings -> Pages**.
4. En **Source** elegi **Deploy from a branch**; en **Branch** poné `main` y carpeta **/ (root)**. Guarda.
5. Espera ~1 minuto. Tu sitio queda online en:
   `https://<tu-usuario>.github.io/trackit/`

### Opcion B - por git (terminal)
```bash
git init
git add index.html README.md
git commit -m "TrackIt landing + demo"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/trackit.git
git push -u origin main
# luego activa Pages en Settings -> Pages (branch: main, root)
```

### Actualizar el sitio
Editas `index.html`, haces commit/push (o subis el archivo de nuevo) y GitHub Pages republica solo.

### Dominio propio (opcional)
**Settings -> Pages -> Custom domain** y agregas el dominio que tengas.

---

## Decisiones de diseño (UX/UI)

- **Color con significado.** La pagina es casi monocromatica (papel calido + tinta + un teal de marca). Los **unicos colores saturados** son los de estado del presupuesto: **verde** = vas bien, **ambar** = cerca del limite, **rojo** = al limite. El color informa, no decora.
- **Marca teal, no el azul SaaS de siempre.** El teal comunica claridad/confianza ("ver con claridad a donde va tu plata") y se diferencia de la competencia.
- **Pantalla de la app en oscuro sobre pagina clara.** Hace que el demo resalte y dirige la mirada al producto.
- **Una sola accion dominante por seccion.** El CTA primario (relleno, alto contraste) no compite con secundarios (ghost). Botones de >=48px de alto: faciles de tocar en mobile.
- **Espacios en blanco generosos.** Las finanzas generan ansiedad; el aire reduce la carga visual y transmite calma. La proximidad agrupa lo que va junto.
- **Tipografia con jerarquia.** Display *Bricolage Grotesque* para titulares; *Inter* con cifras tabulares para los montos (los numeros alinean, clave en finanzas).
- **Piso de calidad.** Responsive hasta mobile, foco visible por teclado, prefers-reduced-motion respetado, HTML semantico y textos en voz activa ("Probar la demo").
