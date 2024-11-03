Here's the revised README with the spinning ASCII donut example:

---

# ASCII Animation Showcase Library

A collection of ASCII animations in C++ that you can easily copy and paste to run in your own projects! Perfect for adding retro-styled animations to your terminal-based applications.

## Features
- Multiple ASCII animations ready to showcase
- Code organized for simple copy-and-paste use
- Each animation includes customizable timing and loop options
- Lightweight and works on all major platforms

## Table of Contents
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Available Animations](#available-animations)
- [Customization](#customization)
- [Contributing](#contributing)

---

## Getting Started

Visit the [GitHub page](https://github.com/username/ascii-animation-showcase) to find individual animations in separate files. Just open a file, copy the code, and paste it into your C++ project.

No need for installation or setup—just copy and enjoy!

---

## Usage

1. **Browse** the animations on the GitHub page.
2. **Copy** the code from any animation file (e.g., `spinning_donut.cpp`).
3. **Paste** it into your project or main file, and run!

### Example

If you want to display a spinning ASCII donut animation:

1. Copy the code from `spinning_donut.cpp`.
2. Paste it into your project, and it’s ready to run.

```cpp
#include <cstdio>
#include <cstring>
#include <cmath>
#include <unistd.h>

int main() {
    float A = 0, B = 0;
    float i, j;
    int k;
    float z[1760];
    char b[1760];
    printf("\x1b[2J");
    for (;;) {
        memset(b, 32, 1760);
        memset(z, 0, 7040);
        for (j = 0; j < 6.28; j += 0.07) {
            for (i = 0; i < 6.28; i += 0.02) {
                float c = sin(i);
                float d = cos(j);
                float e = sin(A);
                float f = sin(j);
                float g = cos(A);
                float h = d + 2;
                float D = 1 / (c * h * e + f);
                float l = cos(i);
                float m = cos(B);
                float n = sin(B);
                float t = c * h * g - f * e;
                int x = 40 + 30 * D * (l * h * m - t * n);
                int y = 12 + 15 * D * (l * h * n + t * m);
                int o = x + 80 * y;
                int N = (int)(8 * ((f * e + c * g * d) * m - c * g * f - e * d - h));
                
                if (22 > y && y > 0 && x > 0 && 80 > x && D > z[o]) {
                    z[o] = D;
                    b[o] = ".,-~:;=!*#$@"[N > 0 ? N : 0];
                }
            }
        }
        printf("\x1b[H");
        for (k = 0; k < 1761; k++) {
            putchar(k % 80 ? b[k] : 10);
        }
        A += 0.00004;
        B += 0.00002;
        usleep(30000);
    }
    return 0;
}
```

---

## Available Animations

- **Spinning Donut:** A mesmerizing rotating 3D donut made with ASCII characters
- **Waving Flag:** A flag rippling in the wind
- **Running Stick Figure:** A stick figure running across the screen
- **Typing Text:** Simulates a typing effect for text
- **Fireworks Display:** A looping fireworks animation

Check out each animation on the GitHub page and simply copy the one you like!

---

## Customization

Each animation is designed to be easy to tweak. You can:
- **Adjust Timing:** Change the frame delay to speed up or slow down the animation.
- **Set Loop Count:** Define the number of repetitions.
- **Edit Frames:** Modify frames directly in the file for custom effects.

---

## Contributing

Have an animation idea? Contributions are welcome:
1. Fork this repository.
2. Add a new animation file with clear comments.
3. Submit a pull request!

Please keep the animations simple and suitable for ASCII display.

---

Enjoy animating with ASCII art! 🎉
