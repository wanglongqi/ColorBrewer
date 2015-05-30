# ColorBrewer
make use of color palette from http://colorbrewer2.org in *Mathematica*

This is my first package written in *Mathematica*. This package provide a simple wrapper for [ColorBrewer](http://colorbrewer2.org).

## Usage

	<<ColorBrewer`
	GetPalette[PaletteName,ColorNumber] 
	(*Get the palette with ColorNumber colors under palette with name PaletteName *)
	CreateColorFunction[PaletteName,ColorNumber]
	(*Get a ColorFunction with ColorNumber colors by palette named PaletteName *)

## Example

	Plot[Evaluate@Table[Sin[i x], {i, 1, 4}], {x, 0, 2 Pi}, 
	 PlotStyle -> GetPalette[Set1, 4]]

![ex1](./demo/ex1.png)

	Plot3D[Sin[x + y^2], {x, -3, 3}, {y, -2, 2}, 
	 ColorFunction -> 
	  Function[{x, y, z}, CreateColorFunction[RdYlBu, 5][z]]]

![ex2](./demo/ex2.png)

You may also use `GetPalette` to check the color palette first, such as 

![pal](./demo/pal.png)

## Feedback

Open an issue in the tracker.

