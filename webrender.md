Files using webrender
- canvas
- canvas_traits

**Inspecting canvas/**

- is using `webrender::api::DirtyRect`
  I've seen this `DirtyRect` a lot in these files.

  It's just an enumeration
  ```rust
  pub enum DirtyRect<T: Copy, U> {
      All,
      Partial(Rect<T, U>),
  }
  ```

and `webrender_api::units::RectExt` is a trait

```rust
pub trait RectExt {
    type Point;
    fn top_left(&self) -> Self::Point;
    fn top_right(&self) -> Self::Point;
    fn bottom_left(&self) -> Self::Point;
    fn bottom_right(&self) -> Self::Point;
}
```

looks like it defines where to paint rectangle, cuz
it has got that 4 points.

Certainly, I got the entry point. It is `ports/glutin/main2.rs`.
There is a lot configuration happening, I don't what but looks so
critical.

At the end, `App::run(do_not_use_native_titlebar, device_pixels_per_px,
user_agent)` which I think is what triggers the browser.

`App` is from `app::App` and that's what you should see.

