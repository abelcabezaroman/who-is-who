## Who is who

Dado el html ``exercise-2.html`` y el css ``exercise-2.css``, crea un archivo de javascript (recuerda que el javascript que
 proporcionamos nosotros es el que contiene la solución propuesta) para crear el famoso juego de Quien es quien!
 
 Para ello abre el fichero ``exercise-2.html`` en tu navegador y verás el resultado final de lo que queremos conseguir. Como ves, tenemos una serie de personas con diferentes caracteristicas fisicas y, debajo una serie de preguntas a
  realizar a nuestro programa. El cometido del programa que hagas será comparar la pregunta seleccionada que haga el
   usuario (botones) y deshabilitar personas en base a si concuerdan con las caracteristicas de la persona a adivinar
    que escogerá aleatoriamente el juego al iniciarse.
    
Deberás programar todas las condiciones partiendo de los **dos arrays que te dejamos al final del README**.
  
##Condiciones

1. Selecciona aleatoriamente una persona del array. Esta es la persona que deberá adivinar el usuario en base a las
 preguntas que haga al juego.  
2. Crea un tablero de juego en el que recorras todas las personas y pinta un ``<img>`` por cada una de ellas con
la imagen que cada persona tiene en la propiedad `.img` dentro
 del ``<div data-function="boardGame">`` 
3. Crea un tablero de preguntas con el array de ``questionsType`` que tendrás al final del README. Por cada uno de
 los objetos de este array deberás pintar un ``<h2>`` con el valor de la propiedad `.title` y tantos botones como
  strings tenga el array de la propiedad ``.questions``. Como consejo, podrás usar la propiedad `.key` para
   posteriormente comparar las respuestas con la persona seleccionada por el juego aleatoriamente.
4. Crea un evento ``click`` en los botones para comprobar si la persona seleccionada aleatoriamente por el juego
 coincide con la opción seleccionada por el usuario. Recorre el array de personas y deshabilita aquellas que no
  coincidan afirmativamente con la comparación. Ej: Si el usuario selecciona la opción ``Yes`` de la pregunta ``Glasses
tendremos que comprobar que el usuario seleccionado aleatoriamente por el juego tiene gafas...en caso de que las
 tenga. Deshabilitamos todos las personas que no tengan gafas y, en caso de que no la tenga, lo contrario. Para
  deshabilitar te recomendamos que añadas el estilo `pointers-events: 'none'` y `opacity: '0.2'`. Deshabilita también
   el botón al que el usuario ha hecho click con las mismas propiedades para que no pueda volver a
   darle. Finalmente, suma 1 al contador de pistas que estará en el `<span data-function="clueCount""`.
  5. Una vez hecho esto el usuario tendrá la capacidad de jugar hasta que decida que sabe quien es la persona
   seleccionada aleatoriamente por el juego. Para que el usuario seleccione la persona que cree que es, añade un
    evento `click` a las imagenes que comprueben si esa persona es realmente la persona que el juego ha seleccionado
    . Si es, crea una alerta felicitando al usuario por ganar con el numero de pistas usadas y si no...saca una
     alerta pero con un mensaje un poco menos optimo...you lose :(. Este evento sería lo ideal que lo hicieras
      al crear el tablero de juego con las personas...por optimizar jeje.
  6. Por último para nota, resetea el juego cuando el usuario elija una persona como respuesta. Para que pueda volver
   a jugar, basicamente :)
##Recursos

```js
const questionsType = [
    {
        title: 'Gender',
        key: 'gender',
        questions: ['Man', 'Woman']
    },
    {
        title: 'Hair Color',
        key: 'hairColor',
        questions: ['Blonde', 'Red', 'Pink', 'Brown', 'White', 'Black']
    },
    {
        title: 'Moustache',
        key: 'moustache',
        questions: ['Yes', 'No']
    },
    {
        title: 'Glasses',
        key: 'glasses',
        questions: ['Yes', 'No']
    },
    {
        title: 'Hat or Cap',
        key: 'hatOrCap',
        questions: ['Yes', 'No']
    },
    {
        title: 'Clothes color',
        key: 'clothesColor',
        questions: ['Red', 'Orange', 'Green', 'White', 'Black', 'Pink', 'Red']
    },
    {
        title: 'Skin color',
        key: 'skinColor',
        questions: ['Light', 'Dark']
    },
    {
        title: 'Long Hair',
        key: 'longHair',
        questions: ['Yes', 'No']
    }
]

const persons = [
    {
        img: 'public/001-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/002-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/003-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Green',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/004-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'Yes',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/005-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/006-man.svg',
        gender: 'Man',
        hairColor: 'Brown',
        moustache: 'Yes',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Green',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/007-man.svg',
        gender: 'Man',
        hairColor: 'Red',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/008-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/009-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/010-woman.svg',
        gender: 'Woman',
        hairColor: 'Brown',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/011-woman.svg',
        gender: 'Woman',
        hairColor: 'Dark',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/012-woman.svg',
        gender: 'Woman',
        hairColor: 'Red',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/013-woman.svg',
        gender: 'Woman',
        hairColor: 'White',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/014-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/015-woman.svg',
        gender: 'Woman',
        hairColor: 'Brown',
        moustache: 'No',
        glasses: 'Yes',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/016-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'Yes',
        clothesColor: 'Pink',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/017-woman.svg',
        gender: 'Woman',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/018-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/019-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/020-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/021-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'Yes',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/022-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'Yes',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/023-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/024-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/025-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/026-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/027-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/028-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/029-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/030-woman.svg',
        gender: 'Woman',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Orange',
        skinColor: 'Dark',
        longHair: 'No'
    }, {
        img: 'public/031-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Green',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/032-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'Yes',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/033-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/034-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Dark',
        longHair: 'Yes'
    }, {
        img: 'public/035-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/036-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/037-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'Yes',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/038-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/039-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'Yes',
        glasses: 'No',
        hatOrCap: 'Yes',
        clothesColor: 'Green',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/040-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/041-man.svg',
        gender: 'Man',
        hairColor: 'Blonde',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/042-man.svg',
        gender: 'Man',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Red',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/043-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Black',
        skinColor: 'Light',
        longHair: 'Yes'
    }, {
        img: 'public/044-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'Pink',
        skinColor: 'Light',
        longHair: 'No'
    }, {
        img: 'public/045-woman.svg',
        gender: 'Woman',
        hairColor: 'Black',
        moustache: 'No',
        glasses: 'No',
        hatOrCap: 'No',
        clothesColor: 'White',
        skinColor: 'Light',
        longHair: 'No'
    }
]
```
