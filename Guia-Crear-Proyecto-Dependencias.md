
# GUÍA PARA CREAR UN PROYECTO E INSTALAR DEPENDENCIAS

## 1. Comprobar Node.js y npm

```bash
node -v
npm -v
```

## 2. Crear un proyecto React

```bash
npx create-react-app MiProyecto
cd MiProyecto
npm start
```

## 3. Instalar dependencias

### React Router

```bash
npm install react-router-dom
```

### Axios

```bash
npm install axios
```

### Bootstrap

```bash
npm install bootstrap
```

Si el ejercicio utiliza la configuración antigua de Bootstrap con jQuery y Popper.js:

```bash
npm install jquery popper.js
```

### Tailwind CSS v3

```bash
npm install -D tailwindcss@3
npx tailwindcss init
```

## 4. Instalar dependencias de un proyecto descargado

Si el proyecto ya existe y contiene `package.json`, entramos en su carpeta y ejecutamos:

```bash
npm install
```

Para iniciarlo:

```bash
npm start
```

## 5. Resumen rápido

| Necesidad | Comando |
|---|---|
| Crear proyecto React | `npx create-react-app MiProyecto` |
| React Router | `npm install react-router-dom` |
| Axios | `npm install axios` |
| Bootstrap | `npm install bootstrap` |
| jQuery y Popper.js (configuración antigua) | `npm install jquery popper.js` |
| Tailwind CSS v3 | `npm install -D tailwindcss@3` |
| Configurar Tailwind v3 | `npx tailwindcss init` |
| Instalar dependencias existentes | `npm install` |
| Iniciar proyecto | `npm start` |
