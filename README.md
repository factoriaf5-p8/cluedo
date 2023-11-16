# JS | Cluedo - Mezclando objetos y arrays

El clásico juego de detectives

Cluedo o Clue es un juego de mesa popular que fue producido originalmente por la empresa Parker Brothers y ha sido uno de los juegos favoritos de generaciones de familias. El objetivo del juego es resolver un caso de asesinato preguntando: ¿quién lo hizo? ¿Con qué arma? ¿En qué habitación? Luego, cada vez que haces una sugerencia en cuanto al posible sospechoso, arma y habitación, vas eliminando las posibilidades y acercándote cada vez más a la verdad.

![Clue Picture](https://i.imgur.com/AZWieq9.jpg)

## Requisitos

- Clona el repo asignado a tu área de trabajo local
- Una vez resuelto:

```
$ git add .
$ git commit -m "done"
$ git push origin main
```

## Ejercicio

1. Abre el fichero de test `SpecRunner.html` con [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).
2. Escribe el código JavaScript en el fichero `src/clue.js`.
3. Comprueba en tu navegador que los tests van pasando (si lo necesitas refresca la página de los tests)


## Iteración 1 - <small>Crear las cartas</small>

El Cluedo tiene tres tipos de cartas: *suspects*, *rooms*, and *weapons*. Los tres tipos de cartas siempre están separadas.

Para hacer esto, necesitarás conocer a los personajes (posibles asesinos), armas disponibles y habitaciones de la casa. Toda la información se encuentra disponible en el fichero `clue.js`.

### Personajes

Todos los personajes tienen nombre, apellido, trabajo, edad, descripción e imagen.

### Armas disponibles

Hay nueve armas.

### Habitaciones

El juego representa el plano de una mansión y describe 15  habitaciones diferentes.

### Estructura de los datos

Crea una estructura de datos para cada uno de los personajes, armas y habitaciones. Cada documento tendrá toda la información.

Cuando hayas creado estas estructuras sube cada documento a su array correspondiente.

Por ejemplo:

```javascript
// Characters Collection
const mrsPeacock = {name: "Peacko", edad:33}
const charactersArray = [mrsPeacock,...];

// Rooms' Collection
const dinningRoom  = {name:"Dinning Room"}
const roomsArray = [dinningRoom,...];

// Weapons Collection
const rope = {name: "rope",weight: 10}
const weaponsArray = [rope,...];
```
Tendrás tres arrays: `charactersArray`, `weaponsArray` y `roomsArray`.

## Iteración 2 - <small>Crea el misterio</small>

Al inicio del juego, los jugadores barajan los mazos de cartas para crear combinaciones de *suspect*, *weapon* y *room*. Este será el misterio a resolver.

### Random Selector

Crea una función `randomSelector` que seleccione de forma aleatoria un elemento del mazo de cartas. El método recibe un `array` como argumento y devuelve un elemento random del array.

### Crea el misterio

Crea una función `pickMistery` que llamará a `randomSelector` por cada mazo de cartas y devolverá un array con tres cartas escogidas: un personaje, un arma y una habitación.

## Iteración 3 - <small>Descubrir el misterio</small>

Para revelar el misterio se ha de crear una función `revealMistery` que recibirá el array del misterio como argumento y lo devolverá revelado con este formato:

**\<FIRST NAME\> \<LAST NAME\> killed Mr.Boddy using the \<WEAPON\> in the \<PLACE\>!!!!**

## Extra Resources

- [20 Mind-blowing facts about Cluedo.](http://whatculture.com/offbeat/20-mind-blowing-facts-you-didnt-know-about-cluedo)
- [Wikipedia](https://en.wikipedia.org/wiki/Cluedo)
- [Data Structures: Objects and Arrays](http://eloquentjavascript.net/04_data.html)