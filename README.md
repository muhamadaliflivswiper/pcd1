# pcd1
import numpy as np 
import imageio.v3 as image

path = "C:/Users/komputer 2/Pictures/Saved Pictures/download.jpg"

image_source = image.imread(path)

if len(image_source.shape) > 3:
    print("Gambar harus dalam mode RGB")
    exit()

red_ch = image_source[:,:,0]
green_ch = image_source[:,:,1]
blue_ch = image_source[:,:,2]
grey_ch = red_ch + green_ch + blue_ch/3

image_red = np.zeros_like(image_source)

image_red[:,:,0] = red_ch
image.imwrite("C:/Users/komputer 2/Documents/muhamadalif/r.jpg", image_red)

image_green = np.zeros_like(image_source)

image_green[:,:,1] = green_ch
image.imwrite("C:/Users/komputer 2/Documents/muhamadalif/r.jpg", image_green)

image_blue = np.zeros_like(image_source)


image_blue[:,:,2] = blue_ch
image.imwrite("C:/Users/komputer 2/Documents/muhamadalif/r.jpg", image_blue)

image_grey = np.zeros_like(image_source)

image_grey[:,:,0] = grey_ch
image_grey[:,:,1] = grey_ch
image_grey[:,:,2] = grey_ch
image.imwrite("C:/Users/komputer 2/Documents/muhamadalif/r.jpg", image_grey)

print("proses selesai dikerjakan")
