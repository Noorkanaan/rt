## 🧱 Raytracer - How to Use

This simple raytracer renders models using camera positions and brightness. You can render a specific object by passing its name as an argument when running the program.

### 🏁 How to Run

Build and run the project in **release mode** for faster performance:

```bash
cargo run --release <object_name>
```

✅ Example:

```bash
cargo run --release cube
```

This will render a cube based on the camera angle in `camera.rs`.

---

### 🎥 Camera Control

Camera settings are **hardcoded** in `camera.rs`:

```rust
let look_from = Vec3::new(...);  // Camera position
let look_at = Vec3::new(...);    // Where the camera looks
```

If you want a **top view**, **side view**, or **front view**, edit the `look_from` and `look_at` values in the `Camera::new()` method.

---

### 💡 Brightness / Lighting

Brightness and shading are affected by light direction and dot product logic. You can tweak this inside main:

```rust
color = (color / (samples_per_pixel as f32)) * 1.5;
```

Change `1.5`, increase to make brighter, and decrease to make it darker.

---

### 🖼 Output

After running the raytracer, the rendered image is saved as:

```
output.png
```

You can view it with any image viewer.

---

