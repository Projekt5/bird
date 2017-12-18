# bird
from pylab import *
from scipy import *
from datetime import *
from astral import *

def testfile():
    file=open('bird_jan25jan16fix.dat','r')
    return file

lista=list(testfile())
print(lista)
lista_tid=[k[0:26] for k in lista]
lista_antal=[k[29:-2] for k in lista]

kommentarer
lista_antal2=[int(k[29:-2]) if isinstance(k,int) else k[29:-2] for k in lista]
listaAntal=[int(k) for k in lista_antal] # funkar inte för alla k? 

nylista=[]
n=0
for k in lista_antal:                         #testar varför/när
    nylista.append(int(k))
    n+=1
    print(n)                                  #ger error när n=4117, lista_antal[4116]='' empty string
print(len(lista_antal),len(lista_antal2))

print(lista_antal[4116]) #lista_antal[4117],lista_antal[4115]

