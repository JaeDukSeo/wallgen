# WallGen
![](https://img.shields.io/badge/Python-3-blue.svg?style=for-the-badge&logo=python)
---
[![](https://img.shields.io/badge/Website-blue.svg?style=for-the-badge)](http://wallgen.subhrajitpy.me/)


Generates HQ poly wallpapers

- Make poly wallpapers over a gradient with random colors, or using custom colors
- Choose different shapes like hexagons, squares, and diamonds apart from triangles
- Apply polygons over a picture
- Make a [video](https://gist.github.com/SubhrajitPrusty/5f303202c615e42e12b1a640322f9fec) with polygonized style
- Dont have `Python`? Use the [website](http://wallgen.subhrajitpy.me) (Limited capabilites)


## Installation

`pip install --editable .`

## Usage

### `wallgen`

```
Usage: wallgen [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  pic     Use a picture instead of a gradient
  poly    Generates a HQ low poly image
  shape   Generates a HQ image of a beautiful shapes
  slants  Generates slanting lines of various colors

```

### `wallgen poly --help`

```
Usage: wallgen poly [OPTIONS] SIDE

  Generates a HQ low poly image

Options:
  -c, --colors TEXT     use many colors custom gradient, e.g -c #ff0000 -c
                        #000000 -c #0000ff
  -p, --points INTEGER  number of points to use, default = 100
  -s, --show            open the image
  -o, --outline         outline the triangles
  -n, --name TEXT       rename the output
  --help                Show this message and exit.

```

### `wallgen shape --help`


```
Usage: wallgen shape [OPTIONS] SIDE

  Generates a HQ image of a beautiful shapes

Options:
  -t, --type [square|hex|diamond]
                                  choose which shape to use
  -c, --colors TEXT               use many colors custom gradient, e.g -c
                                  #ff0000 -c #000000 -c #0000ff
  -s, --show                      open the image
  -o, --outline                   outline the shapes
  -n, --name TEXT                 rename the output
  --help                          Show this message and exit.

```

### `wallgen slants --help`

```
Usage: wallgen slants [OPTIONS] SIDE

  Generates slanting lines of various colors

Options:
  -s, --show       open the image
  -n, --name TEXT  rename the output
  --help           Show this message and exit.

```

### `wallgen pic --help`

```
Usage: wallgen pic [OPTIONS] COMMAND [ARGS]...

  Use a picture instead of a gradient

Options:
  --help  Show this message and exit.

Commands:
  poly   Generates a HQ low poly image
  shape  Generate a HQ image of a beautiful shapes

```

### `wallgen pic poly --help`

```
Usage: wallgen pic poly [OPTIONS] IMAGE

  Generates a HQ low poly image

Options:
  -p, --points INTEGER  number of points to use, default = 1000
  -s, --show            open the image
  -o, --outline         outline the triangles
  -n, --name TEXT       rename the output
  --help                Show this message and exit.
  
```

### `wallgen pic shape --help`

```
Usage: wallgen pic shape [OPTIONS] IMAGE

  Generate a HQ image of a beautiful shapes

Options:
  -t, --type [square|hex|diamond]
                                  choose which shape to use
  -s, --show                      open the image
  -o, --outline                   outline the shapes
  -n, --name TEXT                 rename the output
  --help                          Show this message and exit.
  
```
---

## Usage Docker

Inside the folder

`docker build -t wallgen-doc:latest .`

`docker run -d -p 5000:5000 wallgen-doc`

Run `docker ps` to check if container is running.

Goto [localhost:5000](http://localhost:5000) to check out the website.

---

## Examples


### `wallgen poly 2000`

Random Gradient

<img src="./images/demo1.png" width="50%">

### `wallgen poly 1000 --colors "#ff0000" --colors "#00ddff"`

Fixed color/gradient

<img src="./images/poly.png" width="50%">

### `wallgen poly 2000 -c "#dd0000" -c "#4455ff" --points 50`

Fixed no. of points

<img src="./images/demo9.png" width="50%">

### `wallgen poly 2000 -c "#dd0000" -c "#4455ff" -p 500`

Fixed no. of points

<img src="./images/demo8.png" width="50%">

### `wallgen poly 2000 -c "#ff0000" -c "#000000" -c "#0000ff"`

More than 2 colours

<img src="./images/demo3.png" width="50%">

### `wallgen poly 1000 -c "#ff0000" -c "#00ddff" -o "#2c2c2c"`

With outline

<img src="./images/poly-outline.png" width="50%">

### `wallgen shape -t square -c "#ff0099" -c "#00ddff"`

Square pattern

<img src="./images/square.png" width="50%">

### `wallgen shape -t square -c "#ff0099" -c "#00ddff" -o "#2c2c2c"`

Square pattern with Outline

<img src="./images/square-outline.png" width="50%">

### `wallgen shape -t hex -c "#ff0099" -c "#00ddff"`

Hexagon pattern

<img src="./images/hex.png" width="50%">

### `wallgen shape -t hexagon -c "#ff0099" -c "#00ddff" -o "#2c2c2c"`

Hexagon pattern with Outline

<img src="./images/hex-outline.png" width="50%">

### `wallgen shape -t diamond -c "#ff0099" -c "#00ddff"`

Diamond pattern

<img src="./images/diamond.png" width="50%">

### `wallgen shape -t square -c "#ff0099" -c "#00ddff" -o "#2c2c2c"`

Diamond pattern with Outline

<img src="./images/diamond-outline.png" width="50%">

### `wallgen slants 2000`

Slants pattern

<img src="./images/demo6.png" width="50%">

### `wallgen pic poly lion.jpg -p 50000`

Using a picture with 50000 points

1

<img src="./images/lion.jpg" width="50%">
<img src="./images/lion-poly.png" width="50%">

2

<img src="./images/anime.png" width="50%">
<img src="./images/anime-poly.png" width="50%">

3

<img src="./images/clouds.jpg" width="50%">
<img src="./images/clouds-poly.png" width="50%">



## Screenshots

### Homepage

![homepage](./images/web-home.png)

### Poly Page

![Polygon](./images/web-poly.png)

### Shapes Page

![Polygon](./images/web-shape.png)