# Step 3: Hardware Assembly

Now it's time to build your robot! Choose one of two designs: a **Driving Robot** or a **Tilty Robot**. As a team, pick which one you want to build.

| Driving Robot | Tilty Robot |
|---------------|-------------|
| A wheeled mobile robot | A pan/tilt dashboard robot |

## Option A: Driving Robot

### Assembly

1. Screw the axle piece to a motor.
2. Insert the axle into the wheel.
3. Build a base with cardboard.
4. Attach 2 Dynamixel motors and a roller ball to the base. The wheels should form a triangle with the roller ball.

### Upload Drive Mode

5. Edit `platformio.ini`: comment out `+<2motor.cpp>` and uncomment `+<drive.cpp>`:
   ```ini
   ;+<2motor.cpp>
   +<drive.cpp>
   ;+<tilty.cpp>
   ```
6. Upload the new firmware by pressing the **arrow button (->)** at the bottom of VS Code.

### Connect and Drive

7. Connect your phone to the WiFi network with your name (ignore "no internet" warnings).
8. Go to the URL shown in the Serial Monitor (e.g., `https://192.168.XX.YY/drive.html`). If you don't see it, press the reset button on the TinyPICO.
9. Press the **Activate** toggle and drive your robot!

---

## Option B: Tilty Robot

### Prepare Motors

1. Connect your phone to the WiFi network. Go to the 2-motor control page (e.g., `https://192.168.XX.YY/2motor.html`).
2. Set **both motors to position 0**. The motors need to be in this position for correct assembly.

### Assembly

3. Attach the robot "head" to **motor 1**: screw up through the hinge bracket into the small holes on the motor front. The head should be "looking" forward while in the 0 position.
4. Take **motor 2** and attach *just* the idler and idler cap.
5. Attach the head and hinge assembly to motor 2. The LED at the top of motor 2 should face you. **Do not rotate the wheels from the 0 position!**

### Upload Tilty Mode

6. Edit `platformio.ini`: comment out `+<2motor.cpp>` and uncomment `+<tilty.cpp>`:
   ```ini
   ;+<2motor.cpp>
   ;+<drive.cpp>
   +<tilty.cpp>
   ```
7. Upload the new firmware by pressing the **arrow button (->)** at the bottom of VS Code.

### Connect and Play

8. Connect your phone to the WiFi network with your name (ignore "no internet" warnings).
9. Go to the URL shown in the Serial Monitor. If you don't see it, press the reset button.
10. Press the **Activate** toggle and play with your tilty robot!

---

**Next step:** [Interaction Design](04_interaction.md)
