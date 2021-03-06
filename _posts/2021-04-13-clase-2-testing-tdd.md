---
title: 'Clase 2 - Pruebas automatizadas y TDD'
date: 2021-04-13
author: faloi
categories: [Clases]
tags: [kotlin, tdd, pruebas]
videos:
  - id: DxGPT2v19ac
    nombre: Encuentro sincrónico del 14 de Abril
    descripcion: >
      Hablamos de los errores comunes de la clase anterior y presentamos esta clase.
  - id: 8MGtLPFtbQ8
    nombre: Introducción veloz a TDD
    descripcion: >
      Breve introducción conceptual a TDD - la técnica que vamos a trabajar esta clase.
  - id: MIb0FHaR_pc
    nombre: ¿Cómo hacer TDD en Kotlin?
    descripcion: >
      Práctica en vivo de TDD sobre el ejercicio Caralibro. El código que viene con el ejercicio de esta clase fue elaborado en ese video, de forma tal que van a poder ver cómo es la práctica.
  - id: FNtBNEVoKSk
    nombre: "Herencia en Kotlin: atributos, métodos y algunos trucos más"
    descripcion: >
      Aclaraciones varias sobre la sintaxis de Kotlin, que les van a servir para este y los próximos ejercicios.
  - id: YdSQ7UEAh5U
    opcional: true
    nombre: Tipos anulables
    descripcion: >
      Seguramente viste que en Kotlin existen tipos métodos que devuelven `Int?` o `Vendedor?`. En este video te explicamos qué son y para qué sirven estos tipos.
  - id: U-U-qiV3P0k
    opcional: true
    nombre: Resolución del ejercicio "Vendedores"
    descripcion: >
      Una solución posible del ejercicio de la clase 1, que puede servirles también para ver a alguien más programando en Kotlin. Por motivos ajenos a la administración, solo está resuelto el código, no hay ningún test ni en el video ni en GitHub. :man_shrugging:
  - id: q5uOdrwR3Lw
    opcional: true
    nombre: Cómo ver las correcciones en GitHub
    descripcion: >
      Gracias a Pablo Méndez, les acercamos un pequeño video-tutorial de cómo ver, comentar o protestar por las correcciones que les hacemos.
lecturas:
  - url: http://wiki.uqbar.org/wiki/articles/testeo-unitario-avanzado.html
    title: Ejemplo de elaboración de casos de prueba
    summary: >
      Con un pequenísimo enunciado, el artículo cuenta paso a paso cómo armar los escenarios de prueba. Ojo :eyes:: las porciones de código están hechas para Xtend y Junit, tecnología que no utilizamos en la materia. Les queda como tarea pensar cómo traducir eso a Kotlin y Kotest.
  - url: https://docs.google.com/document/d/1Q_v48gZfRmVfLMvC0PBpmtZyMoALbh11AwmEllP__eY/edit
    title: Introducción al Testeo Unitario Automatizado
    opcional: true
    summary: >
      Apunte basado en Wollok, que sirve como introducción al testeo automatizado en general. Omitiendo los detalles sobre Wollok, sugerimos su lectura para responder preguntas como ¿por qué es recomendable hacer pruebas unitarias? ¿cómo hacer buenos tests? ¿cuántas cosas debo probar en cada test?
entrega:
  fecha: "2021-04-27 23:59"
  ejercicios:
  - nombre: Caralibro
    descripcion: >
      Aunque el enunciado no lo dice, es **obligatorio** resolver el ejercicio utilizando la práctica TDD. Como siempre, aconsejamos resolver de a un requerimiento a la vez, en este caso comenzando por sus pruebas. Recuerden que este trabajo debe realizarse en parejas, que deben estar conformadas _antes_ de clonar el ejercicio, ya que el sistema arma un repositorio para cada equipo.
    repo: obj2-unahur/caralibro
    classroom: https://classroom.github.com/g/LDdqtwJk
---

En esta clase hablaremos sobre pruebas automatizadas y [_test driven development (TDD)_](https://es.wikipedia.org/wiki/Desarrollo_guiado_por_pruebas), una práctica que nos invita a desarrollar escribiendo primero las pruebas y luego el código.

## Objetivos de la clase

* Conocer la práctica TDD y sus principales lineamientos.
* Aplicar la práctica TDD en un ejercicio de programación.
* Adquirir herramientas para poder elaborar escenarios de prueba.

## ¿Primero las pruebas o el código?

Probablemente, la técnica que hasta hoy conocen (y practican) a la hora de programar consiste en escribir código y luego, con algo de suerte, probarlo para ver si efectivamente hace lo que tiene que hacer. A su vez, esta prueba puede ser **manual** (por ejemplo, mediante un _REPL_ o sencillamente apretando botones) o **automatizada** (mediante pruebas unitarias, end-to-end, lo que sea).

Esta clase les propone algo que puede resultar disruptivo y, por qué no, hasta molesto (al menos al principio): comenzar por las pruebas y **luego** escribir el código necesario para que ellas pasen. No ahondaremos aquí en las ventajas y desventajas de la práctica (hay mucho escrito [en internet](https://is.gd/pDaLjc)) pero sí diremos que TDD es una muy buena forma de encarar un problema que no tenemos mucha idea de cómo resolver, y de poner especial atención a las pruebas automatizadas... lo cual nos interesa especialmente en este momento. :smiley:
