# 🌐 UAO - Red Empresarial mediante Grafos y Optimización de Rutas

[![UAO](https://img.shields.io/badge/Universidad-Aut%C3%B3noma_de_Occidente-red?style=for-the-badge&logo=academia)](https://www.uao.edu.co/)
[![Materia](https://img.shields.io/badge/Asignatura-Estructura_de_Datos_2-blue?style=for-the-badge)](https://github.com/EduardCY/UAO-EDA2-Red-Empresarial-Grafos)
[![React](https://img.shields.io/badge/Frontend-React_19_+_Tailwind_4-38B2AC?style=for-the-badge&logo=react)](https://react.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![CI Build](https://img.shields.io/badge/CI-Passing-brightgreen?style=for-the-badge&logo=githubactions)](.github/workflows/ci.yml)
[![Author](https://img.shields.io/badge/Author-Eduard_Criollo_Yule-purple?style=for-the-badge&logo=github)](https://github.com/EduardCY)

> **Plataforma interactiva de análisis de redes de telecomunicación y logística empresarial**, con cálculo de ruta más corta (**Algoritmo de Dijkstra**), árbol de recubrimiento mínimo (**Prim / Kruskal**) y visualización topológica en tiempo real.

---

## 🎯 Arquitectura de la Solución

El sistema modela una infraestructura de sedes empresariales representadas como un grafo ponderado $G = (V, E)$, donde:
* $V$ representa las sedes físicas, datacenters y sucursales.
* $E$ representa las troncales de red con latencia, ancho de banda y costos asociados.

---

## 🏛️ Topología de Red y Enrutamiento Óptimo

```mermaid
graph LR
    SedeP["Sede Principal (Cali)"]
    DC["Datacenter Principal"]
    SucN["Sucursal Norte"]
    SucS["Sucursal Sur"]
    Hub["Hub Logístico"]

    SedeP -- "12 ms / 1 Gbps" --> DC
    SedeP -- "25 ms / 500 Mbps" --> SucN
    DC -- "18 ms / 1 Gbps" --> SucS
    SucN -- "15 ms / 300 Mbps" --> Hub
    SucS -- "20 ms / 400 Mbps" --> Hub
    DC -- "8 ms / 10 Gbps" --> Hub
```

---

## ⚡ Algoritmos de Grafos Implementados

| Algoritmo | Propósito Operativo | Complejidad Temporal | Complejidad Espacial |
|---|---|---|---|
| **Dijkstra** | Ruta con mínima latencia entre sedes | $O((V + E) \log V)$ | $O(V)$ |
| **Prim** | Diseño de red troncal de costo mínimo (MST) | $O(E \log V)$ | $O(V)$ |
| **Kruskal** | Unión de componentes disjuntas mediante DSU | $O(E \log E)$ | $O(V)$ |
| **Matriz de Adyacencia** | Consulta instantánea de adyacencia | $O(1)$ | $O(V^2)$ |
| **Lista de Adyacencia** | Representación eficiente de grafos dispersos | $O(grado(u))$ | $O(V + E)$ |

---

## 🚀 Instalación Rápida

```bash
git clone https://github.com/EduardCY/UAO-EDA2-Red-Empresarial-Grafos.git
cd UAO-EDA2-Red-Empresarial-Grafos

npm install
npm run dev
```

---

## 👨‍💻 Autor

* **Autor:** Eduard Criollo Yule ([@EduardCY](https://github.com/EduardCY))
* **Licencia:** [MIT](LICENSE).
