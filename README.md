# Flowpad

A beat sketchpad for your phone or computer. Record a loop on 16 pads, hit **Next idea**, and keep going. Every idea is saved so you can chain them later.

## Files

- `flowpad.html`: the app. This is the only file you edit.
- `build.sh`: turns `flowpad.html` into `index.html`, the installable site.
- `index.html`: generated. Don't edit it by hand.
- `manifest.webmanifest`, `sw.js`, `icons/`: make it installable and let it open with no signal.

## Run it on this computer

```bash
./build.sh && python3 -m http.server 8765
```

Then open http://localhost:8765 in Chrome. The microphone works on localhost.

## Put it on your phone

The site is hosted on GitHub Pages. Open the Pages address in Chrome on your phone, then use the menu's **Add to Home screen** (or **Install app**). It opens fullscreen like a normal app.

After changing `flowpad.html`:

```bash
./build.sh && git add -A && git commit -m "Update Flowpad" && git push
```

Pages updates within a minute or two.

## Where your stuff is saved

Your ideas, takes and samples are saved in the browser on the device you use. The phone and the computer each keep their own copy.
