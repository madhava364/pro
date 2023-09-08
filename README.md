# pro
import numpy as np 
import matplotlib.pyplot as plt from skimage 
import io

im=io.imread('hum.jpg') 
fig=plt.figure(figsize =(10, 16))

plt.subplot(3,1,1) plt.hist(im[:,:,0].ravel(),256,color='red') 
plt.xlabel('frequency ') 
plt.ylabel('intensities')
plt.title('channel 0')

plt.subplot(3,1,2)
plt.hist(im[:,:,1].ravel(),256,color='blue') 
plt.xlabel('frequency')
plt.ylabel('intensities')
plt.title('channel 1')

plt.subplot(3,1,3) 
plt.hist(im[:,:,2].ravel(),256,color='green') 
plt.xlabel('frequency') 
plt.ylabel('intensities') 
plt.title('channel 2')

plt.tight_layout()
plt.show()
