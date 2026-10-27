# Respuestas del Deber 3

1. En la fase roja falló la prueba que usaba una propina de 150. Se esperaba el mensaje `La propina no puede superar el 100%`, pero la aplicación devolvía `La propina debe estar entre 0 y 100`. Era importante verlo antes de implementar la solución porque confirmaba que la prueba detectaba el problema real y mostraba exactamente qué comportamiento debía corregirse.

2. Durante la demostración temporal, `flutter analyze` detectó el aviso `unused_local_variable`, causado por una variable local que no se utilizaba. La IA también identificó como code smell el mapa de estrategias con conversiones forzadas en `lib/main.dart`. El linter no lo detectó porque no era un error de sintaxis ni una regla de lint configurada: era un problema de diseño y complejidad innecesaria que requería revisar el código y su estructura.

3. Se refactorizó el mapa de estrategias con las conversiones `as RedondeoExacto` y `as RedondeoHaciaArriba` en `lib/main.dart`. Se eliminaron el mapa y los casts, y se usaron directamente instancias concretas de cada estrategia. Después de la refactorización, las 33 pruebas existentes pasaron, por lo que se comprobó que el comportamiento se mantuvo.

4. El archivo con menor cobertura entre los que aparecen en el informe fue `lib/main.dart`, con 84,62 %: se ejecutaron 11 de sus 13 líneas ejecutables. Esto no significa necesariamente que el archivo tenga errores; solo indica que algunas líneas no fueron recorridas por las pruebas. Además, tres archivos de `lib/` no aparecen en `coverage/lcov.info`, así que no se les puede asignar un porcentaje a partir de ese informe.
