# 01 · Blink an LED

**Date:** Oct 12, 2026
**Stage:** 1 (my very first program)
**Code:** [`Blink/Blink.ino`](Blink/Blink.ino)

## What it does

Turns the little LED marked **L** on the Arduino Uno on for one second, then off for one second, forever. That LED is wired to pin 13 inside the board, so no extra parts are needed.

## Parts

- Elegoo Uno R3
- USB cable

## How the code works

| Line | What it means |
|---|---|
| `void setup() { ... }` | Runs **once** when the board turns on. |
| `pinMode(LED_BUILTIN, OUTPUT);` | Sets the LED's pin to send power out instead of reading it in. |
| `void loop() { ... }` | Runs **over and over** forever. |
| `digitalWrite(LED_BUILTIN, HIGH);` | Turns the pin on (5 volts), so the LED lights. |
| `delay(1000);` | Waits 1000 milliseconds, which is 1 second. |
| `digitalWrite(LED_BUILTIN, LOW);` | Turns the pin off (0 volts), so the LED goes dark. |

## What I changed

I changed the `delay` numbers and predicted what would happen before uploading. I learned that the on time and the off time are separate. Each `digitalWrite` has its own `delay`.

<!-- Write which numbers you tried, what you predicted, and what actually happened. -->

## What went wrong and how I fixed it

- **Missing `}`**: the code wouldn't compile because a curly bracket was missing. Every `{` needs a matching `}`.
- **"Unable to open port COM3"**: the upload failed because something else was using the port.
- **Verify vs Upload**: I mixed them up at first. ✓ Verify only checks the code. → Upload checks it *and* sends it to the board.

## In my own words

<!-- 2 or 3 sentences: how it felt to see your first program run, and what you'd tell someone starting from zero. -->

## Photo / video

<!-- Drag a photo or short clip of the blinking board in here. -->
