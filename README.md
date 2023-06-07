# Laboratorio 6

Objetivo:
En esta práctica diseñarás e implementarás un contador binario de 10 bits que a la salida muestra el valor de la cuenta en 10 ledes. De manera predeterminada, el contador aumentará su cuenta cada segundo. Al oprimir un botón, el contador cambiará su modo y trabajará en modo descendente. Si el botón vuelve a presionarse, entonces el contador regresará al modo ascendente.
A su vez, el contador podrá aumentar su velocidad x2, x4 y x8 al oprimir un segundo botón. La velocidad regresará a x1.

#Exti_isr.


Se tiene para SysTick_CTRL para desactivar SysTick IRQ y SysTick TIMER. Ya que se activo los flancos de subida ahora se desactivan los de bajada  y se especifica los ciclos de reloj en tre las interrupciones una vez se limpia el valor de systick val se estable ahora la interrupcion.Al colocar el  SysTick_CTRL sirve para activar SysTick timer y SysTick interrupt


#Systick:
Es un temporizador donde hace una cuenta que incrementa y decrementa. Una interrupción externa es aquella que es disparada por una señal generada por un periférico externo al µC, por ejemplo, el cambio de voltaje generado al oprimir un botón. Las interrupciones externas de la cero a la cuatro están asociadas a su propia ISR, mientas que las interrupciones de en los rangos [9, 5] y [15, 10] se atienden mediante la misma ISR cada una. El temporizador del sistema (*SysTick*) es un contador de 24 bits que genera una excepción cada que la cuenta llega a cero y se reinicia. Para configurar la funcion systick se necesita 
habilita el contador.

Para habilitar la interrupción de SysTick, el programa necesita configurar tres bits y luego se establece el bit TICKINT en SysTick_CTRL para habilitar la interrupción de SysTick.Habilite la interrupción SysTick en el vector NVIC. Tenga en cuenta que SysTick la interrupción está habilitada de forma predeterminada en el vector NVIC.

#Oput
Esta configurado para que se puedan hacer el conteo es donde se hablitan los 10 leds.
#Congiguracion

Para la configuracion de los puertos se toman en este ejemplo los "A" donde se asigana del 0 al 9 los pines de entrada y el A10 y A11 para los botones que haran el decremento y el incremento.

#Comandos
MAKE CLEAN:
para limpiar consola

Make : Para crear los archicos .o (objetos)

Make Write:
Para escribir en la blue pin


![Captura desde 2023-06-07 15-00-51](https://github.com/545Mariana/Lab6/assets/109254012/1899512b-09f5-4e18-9fdf-1c991bc92f11)
