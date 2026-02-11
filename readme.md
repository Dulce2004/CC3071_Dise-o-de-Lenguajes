# [M2] Lab - Fase inicial de un compilador con Lex y Yacc

## Descripción

Este laboratorio implementa la fase inicial de un compilador simple utilizando Lex para el análisis léxico y Yacc para el análisis sintáctico.

El lenguaje desarrollado permite:

- Asignación de variables
- Operaciones aritméticas simples y complejas
- Manejo de errores léxicos
- Experimentación con precedencia de operadores

Todo el flujo se ejecuta dentro de un contenedor Docker para evitar instalaciones locales.

---

## Instrucciones de compilación y ejecución

1. **Ingresar a la carpeta del proyecto**
	```bash
	cd lab-1
	```

2. **Construir la imagen Docker**
	```bash
	docker build --rm . -t lab1-image
	```

3. **Ejecutar el contenedor**
	```bash
	docker run --rm -ti -v "${pwd}:/home" lab1-image
	```

4. **Compilar el lenguaje (dentro del contenedor)**
	```bash
	sh buildLanguage.sh
	```

5. **Ejecutar el compilador (dentro del contenedor)**
	```bash
	./calc
	```

## Ejemplos de uso

```text
x = 5
y = 3 + 4
z = 2 + 3 * 4
x = 5 @ 3
```

## Funcionalidades implementadas

- Asignación de variables
- Evaluación de expresiones aritméticas
- Manejo de precedencia de operadores
- Detección de tokens inválidos

## Recompilación

Si se modifican los archivos del lenguaje ([Lex_Yacc/lab-1/files/simple_language.l](Lex_Yacc/lab-1/files/simple_language.l) y [Lex_Yacc/lab-1/files/simple_language.y](Lex_Yacc/lab-1/files/simple_language.y)) es necesario volver a ejecutar:

```bash
sh buildLanguage.sh
```

## Salir del contenedor

Para salir del entorno interactivo utiliza:

```bash
exit
```





