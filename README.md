# Photon Cannon Defense

[한국어](README.ko.md)

A StarCraft-themed defense game where you protect Photon Cannons from waves of Marines and Wraiths. I made it to see whether drag selection and move orders would work.

<p>
  <img src="docs/screenshots/screenshot-1.png" width="480" alt="Gameplay">
</p>


## How to play

Download it from Releases and run it.

Left-click and drag to select several Zealots at once, then right-click to give a move order. Marines and Wraiths keep coming, so you have to stop them before they destroy the Photon Cannons.

You lose when 3 buildings are destroyed. At 40 kills you get extra resources and a Zealot, and at 80 kills the enemies switch to Wraiths. The window title bar shows the number of destroyed buildings and kills.


## How it works

Drag selection uses two global variables and coordinate comparisons. When the mouse button goes down, the game stores that point's x and y in the global variables and draws the selection box. When the button is released, every Zealot checks whether its own coordinates fall between the stored point and the current mouse point. It makes four comparisons for each drag direction, and if the check passes, it turns itself into the selected Zealot object.

The game tells selected Zealots apart by object type instead of using a variable.


## Files

| Path | Contents |
|---|---|
| `source/photon-cannon-defense.gmk` | Original project file |
| `source/split/` | Text tree produced by GmkSplitter |
| `docs/screenshots/` | Screenshots |
| Releases | Distributed build |


## License

CC BY-NC-ND 4.0. Unmodified copies may be shared for noncommercial purposes with attribution. Distributing modified versions and commercial use are not allowed. Bundled libraries, graphics, sounds, and maps made by other people keep their own rights. See [LICENSE](LICENSE).
