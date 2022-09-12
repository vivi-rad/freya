# Freya 

[![Discord Server](https://img.shields.io/discord/1015005816094478347?logo=discord&style=social)](https://discord.gg/sYejxCdewG)

A GUI library for Rust powered by [Skia](https://skia.org/) and [Dioxus](https://dioxuslabs.com).


```rust

fn app(cx: Scope) -> Element {
    let mut count = use_state(&cx, || 0);

    cx.render(rsx!(
        rect {
            height: "20%",
            width: "100%",
            background: "black",
            padding: "25",
            label { "Number is: {count}" }
        }
        rect {
            height: "80%",
            width: "100%",
            background: "blue",
            padding: "25",
            onclick: move |_| count += 1,
            label { "Increase!" }
        }
    ))
}
```
### Features ✨
- Text, Paragraph
- Containers and rectangles
- Nested scroll views
- Click, mouse move, scroll events
- Background, text color, padding, width, height, min_width, min_height, shadow, border radius, custom layer (like z-index)
- Windows, Linux and MacOS support
- Optional components library
- Animation hooks

### Goals 😁
- Fast
- Lightweight
- Secure
- Full cross platform

### Ideas 💭
- Tauri integration
- Browser-like devtools

## TO-DO 🚧
Besides all the [tracking](https://github.com/marc2332/freya/issues?q=is%3Aopen+is%3Aissue+label%3Atracking) issues, here are some of the things to do:
- [ ] Support for percentages in padding
- [ ] Add `Flex` component (using [taffy](https://github.com/dioxusLabs/taffy)).
- [ ] Documentation
- [ ] Improve Auto calculation for width and height
- [ ] Investigate if `image` diffing can be speeded up (reference: https://github.com/DioxusLabs/dioxus/pull/543#issuecomment-1238393539)
- [ ] Better touchpad support
- [ ] Move layout calculation from the layout engine into the node's state? Not sure.
- [ ] Render shadows one layer below it's element to avoid overlapping with it's siblings

[MIT License](./LICENSE.md)