# scad-preview.el

Preview SCAD models in real-time in Emacs

## Screenshot

![Screenshot](screenshot.png)

## Installation

Install _scad-mode_ and load this script:

    (require 'scad-preview)

Then call *M-x scad-preview-mode* in a _scad-mode_ buffer to open the
preview pane. You can close the pane by calling *scad-preview-mode*
again.

## Customization

The following variables can be customized with *M-x customize-variable*:

- _scad-preview-default-camera-parameters_ : Default parameters for the gimbal camera
- _scad-preview-refresh-delay_ : Delay in seconds until updating preview (default 1.5s)
- _scad-preview-image-size_ : Size of preview image (default 450x450)
- _scad-preview-window-position_ : Position of the preview window (default 'right)
  - If the value is one of 'right, 'left, 'below, or 'above, the
    preview window is split from the current window in the current
    frame.
  - If the value is 'frame, the preview window is created in a new frame.
- _scad-preview-window-size_ : Size in columns(lines) of the preview window (default 65)
- _scad-preview-colorscheme_ : Colorscheme for rendering preview (default "Cornfield")

## Keybindings

You can rotate the preview image with following keys :

- *<right>*, *l*     : rotate+ around z-axis
- *<left>*, *h*      : rotate- around z-axis
- *<up>*, *k*        : decrease distance (zoom in)
- *<down>*, *j*      : increase distance (zoom out)
- *C-<left>*, *C-h*  : rotate+ around y-axis
- *C-<right>*, *C-l* : rotate- around y-axis
- *C-<up>*, *C-k*    : rotate+ around x-axis
- *C-<down>*, *C-j*  : rotate- around x-axis
- *M-<left>*, *M-h*  : translate+ along x-axis
- *M-<right>*, *M-l* : translate- along x-axis
- *M-<up>*, *M*k*    : translate- along z-axis
- *M-<down>*, *M-j*  : translate+ along z-axis
- *r*                : reset view
