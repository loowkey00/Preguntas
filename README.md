Reflexión teórica: Principios de desarrollo robusto y seguro 

Autor:Nicolás Ortega 

Fecha: 08.04.2025 

 

1. El principio SRP (Single Responsibility Principle): Claridad en el diseño 

El SRP (Principio de Responsabilidad Única), parte de los principios SOLID, actúa como un faro para diseñar sistemas mantenibles. Su premisa es simple pero poderosa: 

    "Cada componente (clase, módulo o función) debe tener una única responsabilidad y, por tanto, una única razón para cambiar". 

    Ejemplo práctico: Una clase User debería encargarse solo de la lógica de usuarios, no de enviar correos (eso sería tarea de EmailService). 

    Impacto: Reduce el acoplamiento y facilita las pruebas unitarias. 

 

2. Validación de entradas: La primera línea de defensa (OWASP) 

Validar las entradas del usuario no es opcional; es un requisito de seguridad. Aquí el vínculo con OWASP (Open Web Application Security Project): 

    Riesgos evitados: Inyecciones SQL, XSS, o corrupción de datos. 

    Recomendación OWASP: "Validar, sanitizar y escapar todo input". 

    Beneficio adicional: Asegura la consistencia de los datos (ej.: evitar que un campo "edad" acepte texto). 

 

3. Modularización: Dividir para conquistar 

Separar el código en funciones/clases bien definidas transforma el caos en orden. Ventajas clave: 

    Legibilidad: Código autoexplicativo (ej.: calculateTax() en lugar de un bloque monolítico). 

    Mantenibilidad: Cambios localizados = menos efectos secundarios. 

    Colaboración: Documentación implícita mediante estructura. 

 

4. Clean Code vs. "Código que funciona": La diferencia entre arte y artesanía 

Clean Code 
	

Código que "funciona" 

Legible como prosa (nombres descriptivos, formato consistente). 
	

Críptico, con "magic numbers" y funciones gigantes. 

Preparado para escalar (bajo acoplamiento). 
	

Frágil; pequeños cambios rompen todo. 

Facilita el onboarding de nuevos devs. 
	

Solo lo entiende quien lo escribió. 

Metafora: Es la diferencia entre un libro bien editado y apuntes desordenados. 

 

5. Errores frecuentes al capturar datos por consola (Python) 

    Falta de validación de tipos/rangos: 

    Ejemplo: Permitir edad = -5 (¿Un usuario con edad negativa?). 

    Errores tipográficos (SyntaxError): 

    Como olvidar : en un if o cerrar un paréntesis. 

    Strings vacíos o espacios en blanco: 

    input("Nombre: ") → Si el usuario presiona Enter, el programa continúa con "". 

Solución: Usar bucles while + condiciones para forzar entradas válidas. 

 

Conclusión 

Estos principios no son teóricos abstractos, sino herramientas cotidianas para construir software seguro, maintainable y colaborativo. La diferencia entre un código "que funciona" y uno profesional radica en aplicar estas prácticas deliberadamente. 
