# Sambango Prepa - Próximos Pasos y Guía de Testing

**Fecha:** 17 Febrero 2026  
**Estado Actual:** Iniciada la estructura base del proyecto  
**Rama:** main

---

## 📋 Resumen Actual del Proyecto

Este es un proyecto Vue 3 + Vite + TypeScript para la preparación de Sambango.

### Estado:
- ✅ Repositorio creado en GitHub
- ✅ `package.json` configurado
- ✅ `vite.config.ts` listo
- ✅ `tsconfig.json` en strict mode
- ✅ `App.vue` básico existe
- ⏳ **SIGUIENTE:** Configurar estructura de carpetas y primeros componentes

---

## 🎯 Proximos Pasos Ordenados (Fase 1-2)

### FASE 1 - ESTRUCTURA BASE (ESTA SEMANA)

#### 1. Configurar directorios base
```bash
cd sambango-prepa
mkdir -p src/{components,views,stores,assets,types,composables,utils}
mkdir -p src/assets/{css,images,fonts}
```

**Archivos a crear:**
- `src/main.ts` - Entry point con Pinia + Router
- `src/router/index.ts` - Router configuration (8-10 rutas)
- `src/types/index.ts` - Tipos generales

#### 2. Configurar Pinia stores (3 stores básicos)
```
src/stores/
├── authStore.ts      (autenticación básica)
├── musicStore.ts     (datos de música/eventos)
└── uiStore.ts        (estado UI global)
```

#### 3. Crear componentes base (4 componentes)
```
src/components/
├── Navbar.vue        (navegación principal)
├── Footer.vue        (pie de página)
├── Container.vue     (wrapper responsive)
└── Card.vue          (componente tarjeta reutilizable)
```

#### 4. Crear 2-3 vistas iniciales
```
src/views/
├── HomeView.vue      (landing page)
├── EventosView.vue   (listado de eventos)
└── LoginView.vue     (autenticación)
```

**Tiempo estimado:** 3-4 horas  
**Prioridad:** 🔴 CRÍTICA - Desbloquea todo lo demás

---

### FASE 2 - INTEGRACIÓN BOOTSTRAP (PRÓXIMA SEMANA)

#### 1. Instalar Bootstrap 5
```bash
npm install bootstrap
npm install --save-dev sass
```

#### 2. Estilos base
```
src/assets/css/
├── main.scss         (import de Bootstrap + variables)
├── variables.scss    (theme customizado)
└── utilities.scss    (estilos globales)
```

#### 3. Theme customization
- Variables de color para Sambango
- Tipografía personalizada
- Espaciado Bootstrap modificado

**Tiempo estimado:** 2-3 horas  
**Prioridad:** 🟠 ALTA - Mejora UX rápidamente

---

### FASE 3 - FUNCIONALIDAD CORE (EN 2 SEMANAS)

#### 1. Sistema de autenticación
- Login/Register forms
- Token management (localStorage)
- Protected routes

#### 2. Listado de eventos/música
- API mock con datos Sambango
- Filtros basic (por artista, fecha, género)
- Cards con información

#### 3. Detalles y booking
- Page de detalle de evento
- Sistema de reserva
- Carrito de compra

**Tiempo estimado:** 15-20 horas

---

## 🧪 GUÍA DE TESTING - CÓMO EMPEZAR

### 1. ANTES DE EMPEZAR (Setup Inicial)

```powershell
# Navega al proyecto
cd d:\IONOSHiDrive\users\adela82\adela\proyectos\tic\sambango-prepa

# Instala o verifica dependencias
npm install

# Verifica que todo está correcto
npm run build
```

**Check:** No debe haber errores en la consola

---

### 2. DESARROLLO LOCAL (Comando Principal)

```powershell
# Inicia servidor de desarrollo
npm run dev

# Debería mostrarte:
# > vite
# 
# VITE v5.x.x  ready in xxx ms
# 
# ➜  Local:   http://localhost:5173/
# ➜  press h to show help
```

**Accede a:** http://localhost:5173 en el navegador

---

### 3. TESTING INCREMENTAL

Cada vez que termines de codificar:

#### ✅ Test 1: Sin errores de compilación
```powershell
# En la terminal de Vite (está corriendo con npm run dev)
# Debería estar todo verde, sin errores en rojo
# Abre DevTools: F12 → Console tab → Sin errores rojos
```

#### ✅ Test 2: Componentes cargan
```javascript
// En DevTools console, prueba:
console.log('Vue app loaded')
// Debería ver el mensaje
// Las vistas deberían renderizarse sin issues
```

#### ✅ Test 3: Stores funcionan
```javascript
// Para probar Pinia (cuando esté configurado)
// En console:
import { useAuthStore } from '@/stores/authStore'
const auth = useAuthStore()
console.log(auth.user) // Debería mostrar el estado
```

#### ✅ Test 4: Router funciona
```javascript
// Prueba navegar entre rutas
// Click en links del navbar
// URL debería cambiar sin recargar página
```

---

### 4. CHECKLIST ANTES DE APAGAR

- [ ] `npm run dev` corre sin errores
- [ ] DevTools console sin errores rojos
- [ ] Componentes renderizados en pantalla
- [ ] No hay warnings de TypeScript

---

## 📝 CHECKLIST PARA RETOMAR

### Cuando enciendas el ordenador:

```powershell
# 1. Abre PowerShell/Terminal
# 2. Navega al proyecto
cd d:\IONOSHiDrive\users\adela82\adela\proyectos\tic\sambango-prepa

# 3. Instala dependencias (si es primera vez o tienes conflictos)
npm install

# 4. Inicia desarrollo
npm run dev

# 5. DevTools
# Abre navegador → http://localhost:5173
# F12 → Console
# Verifica: Sin errores rojos
```

---

## 🔧 COMANDOS ÚTILES RÁPIDOS

```powershell
# Desarrollo (el principal)
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview

# Type checking (si necesitas validar TypeScript)
npm run type-check  # Si está configurado

# Limpiar node_modules (si hay conflictos)
rm -r node_modules package-lock.json
npm install
```

---

## 📂 ESTRUCTURA FINAL QUE VAMOS A TENER

```
sambango-prepa/
├── src/
│   ├── components/
│   │   ├── Navbar.vue
│   │   ├── Footer.vue
│   │   ├── Container.vue
│   │   └── Card.vue
│   ├── views/
│   │   ├── HomeView.vue
│   │   ├── EventosView.vue
│   │   └── LoginView.vue
│   ├── stores/
│   │   ├── authStore.ts
│   │   ├── musicStore.ts
│   │   └── uiStore.ts
│   ├── router/
│   │   └── index.ts
│   ├── assets/
│   │   ├── css/
│   │   │   ├── main.scss
│   │   │   ├── variables.scss
│   │   │   └── utilities.scss
│   │   └── images/
│   ├── types/
│   │   └── index.ts
│   ├── composables/
│   ├── utils/
│   ├── main.ts
│   ├── App.vue
│   └── index.html
├── public/
├── package.json
├── vite.config.ts
├── tsconfig.json
├── index.html
└── PROXIMOS_PASOS.md (este archivo)
```

---

## 🎯 TABLA DE PRIORIDADES

| Tarea | Prioridad | Tiempo | Bloqueante | Estado |
|-------|-----------|--------|-----------|--------|
| Configurar directorios | 🔴 CRÍTICA | 15 min | Sí | ⏳ TODO |
| Crear Navbar + Footer | 🔴 CRÍTICA | 45 min | No | ⏳ TODO |
| Pinia stores base | 🔴 CRÍTICA | 60 min | Sí | ⏳ TODO |
| Vue Router | 🔴 CRÍTICA | 45 min | Sí | ⏳ TODO |
| HomeView básica | 🟠 ALTA | 60 min | No | ⏳ TODO |
| Bootstrap + estilos | 🟠 ALTA | 120 min | No | ⏳ TODO |
| Auth system | 🟡 MEDIA | 120 min | No | ⏳ TODO |
| EventosView | 🟡 MEDIA | 90 min | No | ⏳ TODO |

---

## 💡 TIPS PARA TESTING EFICIENTE

### Durante el desarrollo:
1. **Mantén DevTools abierto** - F12 en el navegador
2. **Hot Reload** - Vite recompila automáticamente
3. **Console logs** - Usa `console.log()` para debug
4. **Network tab** - Para ver requests (cuando implementes API)
5. **Vue DevTools** - Extension del navegador para inspeccionar componentes

### Errores comunes:
- ❌ `Cannot find module` → Verifica las imports
- ❌ `Cannot read property 'x' of undefined` → Check null safety
- ❌ `Pinia store not found` → Verifica que está importado en main.ts
- ❌ `Route not found` → Verifica router/index.ts

---

## 📞 REFERENCIAS RÁPIDAS

**Archivos importantes a NO olvidar:**
- `src/main.ts` - Entry point (añadir Pinia y Router aquí)
- `vite.config.ts` - Config de build
- `tsconfig.json` - TypeScript strict: true

**Documentación útil:**
- [Vue 3 Docs](https://vuejs.org)
- [Vite Docs](https://vitejs.dev)
- [Pinia Docs](https://pinia.vuejs.org)
- [Vue Router Docs](https://router.vuejs.org)
- [Bootstrap 5 Docs](https://getbootstrap.com)

---

## ⏹️ RESUMEN FINAL

**Cuando apagues el ordenador:**
- ✅ Este documento está listo para consultar
- ✅ Código está pusheado a GitHub (si usas git)
- ✅ `npm install` ya pasó correctamente

**Cuando enciendas:**
- 🚀 Solo necesitas: `npm run dev`
- 🔍 Sigue el checklist de la sección "PROXIMOS PASOS ORDENADOS"
- 🧪 Usa la "GUÍA DE TESTING" para validar cambios

**Duración estimada de próxima sesión:** 3-4 horas (hasta terminar FASE 1)

---

**¡Muchos éxitos! 🚀 A por ello cuando retomes.** 💪

