from PIL import Image
import numpy as np
import matplotlib.pyplot as plt

Path=r"E:\QQ\Visible\IMG_0412.JPG"
src= Image.open(Path)
r,g,b=src.split()

plt.figure("aaa")

ar=np.array(r).flatten()


plt.hist(ar, bins=256, density =1,facecolor='r',edgecolor='r')  #直方图参数

ag=np.array(g).flatten()

plt.hist(ag, bins=256, density =1, facecolor='g',edgecolor='g')

ab=np.array(b).flatten()

plt.hist(ab, bins=256, density =1, facecolor='b',edgecolor='b')

plt.show()

print(ar[0])
