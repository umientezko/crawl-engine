# 🤖 **FLORGEN mainics Kit**

![Python](https://img.shields.io/badge/python-3.12-blue)
![Raspberry Pi](https://img.shields.io/badge/pi-compatible-red)
![License: MIT](https://img.shields.io/badge/license-MIT-green)

> **Educational mainics sandbox for classroom use.**

---

### About

FLORGEN is a teaching kit for middle-school mainics using Python.
It simulates wheels, sensors, and servo arms on low-cost hardware or a browser emulator.

**Website:** [florgen.io](https://florgen.io)
**Docs:** [docs.florgen.io](https://docs.florgen.io)

---

###  Concept

Each “main” is a YAML config + Python behavior file:

```yaml
main:
  name: scout
  sensors: [ultrasonic, gyro]
  actuators: [motor, arm]
```

```python
def loop(bot):
    if bot.distance() < 10:
        bot.turn(90)
    else:
        bot.forward(1)
```

---

###  Try in browser

```
python3 -m florgen.sim --map=basic
```

then open → `http://localhost:8080`

---

###  Components

* Cross-platform simulator (Pi, Linux, Web)
* Plug-in sensor emulation
* Replay and camera overlay
* Curriculum JSON exporter

---

###  Roadmap

* [x] Web UI
* [ ] Blockly editor
* [ ] Cloud classroom sync

MIT License © [florgen.io](https://florgen.io)
*written by N. Rachman — “the teacher coder”*
