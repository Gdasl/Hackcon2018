# Steg It Up

It isn't as easy as it looks :(

## The Premise

Well we basicallly an image file. As you should always do in this case, we run it through stegsolve. Alpha 0 hits paydirt. We get a series of QR codes,17 to be exact.

## The solving

This was a little disappointing as it was verz straigtforward. All you had to do was to read in each QR code which contained a small part of the flag. I automated the task with the follwing script:

```python
from PIL import Image
import os
from pyzbar.pyzbar import decode
def crop(path, input, height, width, k_, area):
    k = 0
    k = k_
    im = Image.open(input)
    imgwidth, imgheight = im.size
    for i in range(0,imgheight,height):
        for j in range(0,imgwidth,width):
            box = (j, i, j+width, i+height)
            a = im.crop(box)
            try:
                
                a.save(path + 'solvi' + str(k)+'.bmp')
                k +=1
            except Exception as e:
                print e
            


flag = ""
for i in range(17):
    tmp = 'solvi'+str(i)+'.bmp'
    flag+=decode(Image.open(tmp))[0][0]
print stri
```

The flag is: ```d4rk{s000_m4ny_0f_7h3m_l0l_1_h4v33_t0_m4k333_th3_fl4g_l0ng_f0r_n0000_r3450n_1m40}c0de``` 
    
