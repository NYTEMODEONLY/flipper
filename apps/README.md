# Flipper Zero Apps

Custom FAP (Flipper Application Package) apps.

## Creating a New App

Each app needs at minimum:

```
my_app/
├── application.fam    # App manifest (required)
├── icon.png           # 10x10px icon
├── my_app.c           # Your code
└── images/            # Optional assets
```

### Example `application.fam`

```python
App(
    appid="my_app",
    name="My App",
    apptype=FlipperAppType.EXTERNAL,
    entry_point="my_app_main",
    requires=["gui"],
    stack_size=2 * 1024,
    fap_icon="icon.png",
    fap_category="Tools",
)
```

## Building

Install [ufbt](https://github.com/flipperdevices/flipperzero-ufbt):

```bash
pip install ufbt
```

Build your app:

```bash
cd my_app
ufbt
```

Deploy to Flipper:

```bash
ufbt launch
```

## Resources

- [FAP Development Guide](https://developer.flipper.net/flipperzero/doxygen/apps_on_sd_card.html)
- [App Manifests](https://developer.flipper.net/flipperzero/doxygen/app_manifests.html)
- [Flipper Zero Development Toolkit](https://github.com/CodyTolene/Flipper-Zero-Development-Toolkit)
