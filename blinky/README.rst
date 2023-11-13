Blinky
######

Overview
********

This sample is to blink the RGB LEDs. These are the GPIO pins to control the RGB LED.
<br>
#define RED_LED_NODE DT_ALIAS(redled)<br>
#define BLUE_LED_NODE DT_ALIAS(blueled)<br>
#define GREEN_LED_NODE DT_ALIAS(greenled)<br>
<br>
static const struct gpio_dt_spec red_led = GPIO_DT_SPEC_GET(RED_LED_NODE, gpios);<br>
static const struct gpio_dt_spec blue_led = GPIO_DT_SPEC_GET(BLUE_LED_NODE, gpios);<br>
static const struct gpio_dt_spec green_led = GPIO_DT_SPEC_GET(GREEN_LED_NODE, gpios);<br>
<br>
RED   ----- P0.13<br>
BLUE  ----- P0.14<br>
GREEN ----- P0.15<br>

