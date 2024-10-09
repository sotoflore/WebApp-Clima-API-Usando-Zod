# 🌤️ Aplicación de Clima en Tiempo Real

![web app](https://github.com/sotoflore/WebApp-Clima-API-Usando-Zod/blob/main/public/web-app-clima.png)

Una aplicación que proporciona información meteorológica y en tiempo real utilizando la API de [OpenWeather](https://openweathermap.org/). Construida con TypeScript y React, implementando Zod para una validación de tipos robusta y segura.

## 🛠️ Tecnologías Utilizadas
- React + TypeScript
- Zod para validación de tipos
- Axios para peticiones HTTP
- CSS Modules
- OpenWeather API

## 🔍 Uso de Zod para Validación de Tipos
Ejemplo de cómo utilizamos Zod para validar la respuesta de la API:
```ts
const Weather = z.object({
    name: z.string(),
    main: z.object({
        temp: z.number(),
        temp_max: z.number(),
        temp_min: z.number()
    })
})

export type Weather = z.infer<typeof Weather>;
```
