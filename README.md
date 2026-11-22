# RUerererer

[![Android](https://img.shields.io/badge/Platform-Android%2010%20to%2017-3DDC84.svg?style=flat&logo=android)](https://www.android.com/)
[![Graphics](https://img.shields.io/badge/Render-Vulkan%20Mobile%20%7C%20Forward%2B-red.svg?style=flat&logo=vulkan)](https://www.khronos.org/vulkan/)
[![Refresh Rate](https://img.shields.io/badge/Display-30%20to%20240%20Hz-orange.svg?style=flat)](https://github.com/emanuelindustri-source/ruta-1999)
[![Engine](https://img.shields.io/badge/Engine-Godot%204.3%20Mobile-478CBF.svg?style=flat&logo=godot-engine)](https://godotengine.org/)
[![License](https://img.shields.io/badge/License-Proprietary-blue.svg)](LICENSE)
[![Website](https://img.shields.io/badge/Portal%20Web-Live%20Roadmap-yellow.svg)](https://emanuelindustri-source.github.io/ruta-1999/)

> **Conducción Narrativa · Terror Psicológico · Supervivencia Roguelike en Carreteras Venezolanas de 1999.**

---

## 📖 Sinopsis del Juego

En la Venezuela de finales de 1999, tomas el volante de un sedán familiar **Araguaney '99 (1.6L color Beige)** para realizar servicios de traslado interurbano nocturno a través de carreteras desiertas, alcabalas militares y estaciones de servicio abandonadas. 

La atmósfera combina la soledad del asfalto húmedo, lluvia constante, psicofonías en la radio, fallas mecánicas imprevistas y encuentros con criaturas ancestrales del folclore nacional: **El Silbón**, **La Sayona**, **La Loca Luz Caraballo**, y el **Carretón Fantasma de Puerto Cabello**.

---

## 🚗 El Vehículo: Araguaney '99 (1.6L Sedán Beige)

El habitáculo del vehículo está completamente modelado e interactivo:
* **4 Ventanas Eléctricas Independientes:** Control maestro en el reposabrazos del conductor y comandos individuales en copiloto y plazas traseras.
* **Seguros Centralizados:** Bajar los seguros abruptamente altera la reacción y el diálogo de los pasajeros.
* **Luz de Techo:** Manipulable manualmente. Ilumina el interior para revisar mapas, pero atrae la atención de las sombras exteriores.
* **Palanca Automática P-R-N-D-2-L:** Requiere bajar a marcha [2] o [L] en pendientes pronunciadas para evitar el ahogo del motor y el sobrecalentamiento de la transmisión.
* **Guantera Interactiva:** Contiene linterna de metal pesada, mapa físico de rutas, dinero en efectivo (Bolívares) y casetes de música de época.
* **Salida del Vehículo:** Puedes abrir la puerta y salir a pie a examinar el exterior, reparar el radiador sobrecalentado o **esconderte bajo el chasis del carro** si una entidad te acecha.

---

## 🧭 Sensores de Hardware y Dinámica de Control

* **Giroscopio:** Movimiento natural de la cabeza del conductor para mirar hacia los retrovisores, la guantera o el asiento trasero.
* **Acelerómetro:** Opción de volante por inclinación física del dispositivo móvil y sacudidas de cámara ante baches y troneras.
* **Barómetro (Presión Atmosférica):**
  * Al subir de los Llanos hacia el Páramo de Mucuchíes en Mérida (3.450 msnm), la presión atmosférica cae.
  * El motor pierde oxígeno y potencia si no se baja de marcha.
  * Caídas súbitas de presión alertan de la llegada inminente de tormentas eléctricas o fenómenos paranormales antes de ser visibles en la niebla.

---

## 📻 Sistema de Alcabalas, Frecuencia Policial y "Matraca"

* **Escaneo de Banda Corta en la Radio (142.3 MHz):** Permite interceptar las comunicaciones de los puestos de control para saber si *"están tranquilos"*, *"en operativo severo"* o *"matraqueando"*.
* **Control en Alcabala:** Entrega física de Cédula, Carnet de Circulación y Seguro RCV.
* **Consecuencias:**
  * **Negarse a pagar el soborno:** Te retienen a un lado de la vía, revisan la maleta, pierdes tiempo de la noche y aumenta la fatiga del chofer.
  * **Pagar la "Matraca":** Te dejan ir rápido, pero alertan por radio a la siguiente alcabala con tu modelo, color beige y matrícula para extorsionarte de nuevo.
* **Patrullas en Carretera:** Conducir sin luces, a exceso de velocidad o invadiendo canales activa persecución policial con sirenas.

---

## ⚙️ Optimización Multi-SoC y Pantallas 120Hz-240Hz

| Arquitectura SoC | GPU | Perfil de Rendimiento | Tecnologías Activas |
| :--- | :--- | :--- | :--- |
| **Snapdragon 8 Gen 2 / 8 Elite** | Adreno 740 / 830 | Ultra (120-240 FPS) | Snapdragon GSR, Game Mode API, PBR completo |
| **MediaTek Dimensity 9200 / 9400** | ARM Immortalis-G720 / G925 | Alto (120 FPS) | HyperEngine, compresión ASTC 4x4 |
| **Samsung Exynos 2200 / 2400** | AMD RDNA Xclipse / Mali | Alto (90-120 FPS) | Optimizaciones térmicas adaptativas, FSR 1.0 |
| **Unisoc T606 / T616** | Mali-G57 / G52 | Eficiente (30-60 FPS) | Viewport dinámico (720p adaptativo), LODs agresivos |
| **Amlogic (Android TV 32"-80")** | Mali-G31 / G52 MP2 | TV Leanback (60 FPS) | Navegación con control remoto D-Pad y mandos Bluetooth |

* **Física Desacoplada (Fixed DeltaTime a 60 Ticks):** Toda la simulación mecánica y colisiones se procesan de forma independiente de la tasa de cuadros por segundo, permitiendo que pantallas ultra rápidas de 120Hz a 240Hz funcionen con máxima suavidad sin desajustar el comportamiento del carro.

---

## 🗺️ Hoja de Ruta (Roadmap)

- [x] **Fase 1: Fundación & Portal Web Interactivo:** Arquitectura de directorios, GDD maestro, reglas del proyecto y portal web con Web Audio API.
- [x] **Fase 2: Motor Godot 4.3 & Enlace Redmi ADB:** Despliegue de Godot 4.3 portable, proyecto base Vulkan Mobile, validación en Xiaomi Redmi (Android 14) a 120 Hz.
- [ ] **Fase 3: Prólogo del Garaje & Habitáculo 1999:** Modelado e interactividad de mandos, 4 ventanas, seguros, luces y descenso a pie.
- [ ] **Fase 4: Cámaras Duales & Sensores de Hardware:** Conmutador 1ra/3ra persona, giroscopio, acelerómetro y barómetro.
- [ ] **Fase 5: Audio Espacial 3D, Foley & Voces IA:** Sonido del motor 1.6L, radioemisoras y doblaje en español venezolano con 9 idiomas.
- [ ] **Fase 6: Carretera, Climas & Criaturas del Folclore:** Baches procedimentales, tormentas eléctricas, nieve y lógica de IA de El Silbón / Sayona.
- [ ] **Fase 7: Alcabalas, Matraca, Tráfico & Moteles:** Banda policial activa, entregas de documentos, patrullas, gandolas y guardado en moteles.
- [ ] **Fase 8: Menús Multi-SoC, Ajustes FPS & APK Final:** Menú gráfico granular (30-240 FPS), monetización ética Google Play y empaquetado APK.

---

## 🌐 Portal Web Oficial y Roadmap en Vivo

Puedes acceder al portal web interactivo oficial alojado en GitHub Pages:  
👉 **[https://emanuelindustri-source.github.io/ruta-1999/](https://emanuelindustri-source.github.io/ruta-1999/)**

O probarlo localmente ejecutando el script:
```bash
./abrir_portal_web.bat
```

---

## 📜 Licencia y Créditos

* **Desarrollo Integral:** Antigravity AI Engine.
* **Dirección del Proyecto:** Khristyan Hidalgo (@emanuelindustri-source).
* **Inspiración Cultural:** Folclore venezolano, Colección Bicentenario y crónicas populares de carretera.
