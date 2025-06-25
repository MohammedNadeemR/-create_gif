# PyGIF - Python GIF Creator

A simple Python script that creates animated GIFs from a series of PNG images using the imageio library.

## Description

This project takes multiple PNG images and combines them into an animated GIF. The script reads PNG files in sequence and creates a looping GIF with customizable frame duration.

## Features

- Convert multiple PNG images to animated GIF
- Customizable frame duration
- Infinite loop animation
- Simple and lightweight implementation

## Requirements

- Python 3.x
- imageio library

## Installation

1. Clone or download this repository
2. Install the required dependency:
   ```bash
   pip install imageio
   ```

## Usage

1. Place your PNG images in the same directory as `gif.py`
2. Update the `filenames` list in `gif.py` with your image names:
   ```python
   filenames = ['your-image1.png', 'your-image2.png', 'your-image3.png']
   ```
3. Run the script:
   ```bash
   python gif.py
   ```

The script will create a `team.gif` file in the same directory.

## Configuration

You can customize the GIF creation by modifying these parameters in `gif.py`:

- **Duration**: Frame display time in milliseconds (default: 500ms)
- **Loop**: Number of loops (0 = infinite loop)
- **Output filename**: Change 'team.gif' to your desired output name

```python
iio.imwrite('output.gif', images, duration=500, loop=0)
```

## Example

The project includes sample files:
- `team-pic1.png` - First frame
- `team-pic2.png` - Second frame
- `team.gif` - Generated animated GIF

## File Structure

```
pygif/
├── gif.py           # Main script
├── team-pic1.png    # Sample image 1
├── team-pic2.png    # Sample image 2
├── team.gif         # Generated GIF
└── README.md        # This file
```

## How It Works

1. The script imports the imageio library
2. Defines a list of PNG filenames to process
3. Reads each image file and stores it in a list
4. Combines all images into an animated GIF with specified duration and loop settings

## Customization Tips

- **Add more frames**: Simply add more PNG files to the `filenames` list
- **Change speed**: Adjust the `duration` parameter (lower = faster)
- **Different formats**: Modify the script to accept other image formats supported by imageio
- **Reverse animation**: Use `images.reverse()` before creating the GIF

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to fork this project and submit pull requests for any improvements!
