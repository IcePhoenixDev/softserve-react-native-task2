1. Why do we write `onPress={handlePress}` and not `onPress={handlePress()}`?
R:"onPress" necesita una función para ejecutarse cuando es pulsado
2. What is the difference between `Button` and `Pressable`? When would you choose each one?
R: "Button" solo es un botón común y corriente para ser presionado, mientras que "pressable" tiene más opciones de diseño y permite asignarle más funciones
3. What does the `style` function of `Pressable` receive and what does it return? Give an example.
R:La función recibe un objeto con la propiedad pressed, que indica si se está presionando el componente, y devuelve los estilos que se aplicarán según ese estado.
4. Why can you not change a state variable directly (`isFollowing = true`) and what do you do instead?
R: Modificar directamente una variable de estado no notifica a React que debe actualizar el componente. Para hacerlo se utiliza su función actualizadora, como setIsFollowing(true).
5. Why is `followers` not a second `useState`? What is a *derived value*?
R: "followers" puede calcular un estado existente; no hace falta almacenarlo aparte
6. What does *controlled input* mean for `TextInput`? Which two props make it controlled?
R:Significa que React mantiene su valor y lo actualiza cuando el usuario escribe con "value" para el valor actual del campo y "onChangeText" para actualizarlo.
7. Why is `selectedSkills.push(skill)` wrong when `selectedSkills` is state? Write the correct code.
R: Podría modificar el array; es mejor crear uno nuevo en ese caso
setSelectedSkills((current) => [...current, skill]);