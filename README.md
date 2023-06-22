# segundoParcialDomiciliario-SPD

## nombre: :crown: Mariano Lattner :crown:

## Proyecto: Alarma de incendios

![17159508-49e5-489c-8d55-1b2c7e1abc66](https://github.com/marianolattner/segundoParcialDomiciliario-SPD/assets/124000090/ba17b323-dd6e-4c8e-8393-1385b6369582)


## Descripción
El proyecto es una alarma de incendios que dependiendo la epoca del año  y la temperatura ambiente marca si hay un incendio o no ( ademas de marcar la temperatura y la estacion del año en un lcd)

## Funcion principal

esta funcion se encarga de encender la alarma, es decir, de prender los led, prender el servomotor e imprimir "¡INCENDIO! en el led
~~~
void encenderAlarma()
{
    digitalWrite(LED_UNO, HIGH);
    digitalWrite(LED_DOS, HIGH);
    lcd.clear();
    lcd.print("¡INCENDIO!");

    for (int angle = 0; angle <= 180; angle++)
    {
        servoMotor.write(angle);
        delay(15);
    }

    for (int angle = 180; angle >= 0; angle--)
    {
        servoMotor.write(angle);
        delay(15);
    }
    lcd.clear(); // Limpiar la pantalla LCD
}
~~~
## Link al proyecto
- [proyecto](https://www.tinkercad.com/things/11LAY0lFDBX-2-examen-practico-domiciliario-mariano-lattner/editel?sharecode=WzJWj3lSCHW-YfCWBu_iOpk1oPfsNAtHh0nmxgWmQ6A)
