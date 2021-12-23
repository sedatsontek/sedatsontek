# https://github.com/SciSharp/Numpy.NET
# https://www.nuget.org/packages/Numpy/
# https://onegetcdn.azureedge.net/providers/Microsoft.PackageManagement.NuGetProvider-2.8.5.208.dll


import numpy as np
class Fish():

   def __init__(self, year, nugget, sill, range_, name):
        self.year = year
        self.nugget = nugget
        self.sill = sill
        self.range_ = range_
        self.name = name


L = []
L.append(Fish(1967, 0.034, 0.238, 33.917, 'Sardine'))
L.append(Fish(1969, 0.149, 0.087, 33.917, 'Sardine'))
L.append(Fish(1970, 0.074, 0.184, 33.917, 'Sardine'))
L.append(Fish(1971, 0.161, 0.070, 33.917, 'Sardine'))
L.append(Fish(1972, 0.095, 0.157, 33.917, 'Sardine'))
L.append(Fish(2000, 0.053, 0.144, 25.703, 'Sardine'))
L.append(Fish(2001, 0.093, 0.174, 25.703, 'Sardine'))
L.append(Fish(2002, 0.019, 0.197, 25.703, 'Sardine'))
L.append(Fish(2003, 0.066, 0.152, 25.703, 'Sardine'))
L.append(Fish(2004, 0.074, 0.173, 25.703, 'Sardine'))
L.append(Fish(1967, 0.089, 0.233, 136.015, 'Anchovy'))
L.append(Fish(1969, 0.089, 0.186, 136.015, 'Anchovy'))
L.append(Fish(1970, 0.089, 0.088, 136.015, 'Anchovy'))
L.append(Fish(1971, 0.089, 0.016, 136.015, 'Anchovy'))
L.append(Fish(1972, 0.089, 0.191, 136.015, 'Anchovy'))
L.append(Fish(2000, 0.102, 0.097, 45.773, 'Anchovy'))
L.append(Fish(2001, 0.102, 0.162, 45.773, 'Anchovy'))
L.append(Fish(2002, 0.102, 0.175, 45.773, 'Anchovy'))
L.append(Fish(2003, 0.102, 0.213, 45.773, 'Anchovy'))
L.append(Fish(2004, 0.102, 0.075, 45.773, 'Anchovy'))
Sill_=0
Nugget_=0
Range_=0
##0.034, 0.238, 33.917
##0.089, 0.233, 136.015
Nugget = float(input("Lütfen Nugget değerini giriniz: "))
Sill = float(input("Lütfen Sill değerini giriniz: "))
Range = float(input("Lütfen Range değerini giriniz: "))
print(Sill,Nugget,Range)
# for i in range(2):
#
#     for i in range(20):
#         L.append(Fish(L[i].year, round(L[i].nugget + L[i].nugget * 0.1, 6), round(L[i].sill + L[i].sill * 0.1, 6),
#                       round(L[i].ranger + L[i].ranger * 0.1, 6), L[i].name))
#
# for i in range(2):
#
#     for i in range(20):
#         L.append(Fish(L[i].year, round(L[i].nugget - L[i].nugget * 0.1, 6), round(L[i].sill - L[i].sill * 0.1, 6),
#                       round(L[i].ranger - L[i].ranger * 0.1, 6), L[i].name))
#

sardineNuggetToplam=0
sardineNuggetOrtalama=0
sardineSillToplam=0
sardineSillOrtalama=0
sardineRangeToplam=0
sardineRangeOrtalama=0

anchovyNuggetToplam=0
anchovyNuggetOrtalama=0
anchovySillToplam=0
anchovySillOrtalama=0
anchovyRangeToplam=0
anchovyRangeOrtalama=0

sardine_sayac=0
anchovy_sayac=0

for i in range(len(L)):
#print(L[i].year, L[i].nugget, L[i].sill, L[i].ranger, L[i].name)
    if(L[i].name == 'Sardine'):
       sardineNuggetToplam = sardineNuggetToplam +  L[i].nugget
       sardineSillToplam = sardineSillToplam + L[i].sill
       sardineRangeToplam = sardineRangeToplam + L[i].range_
       sardine_sayac = sardine_sayac + 1
    elif L[i].name == 'Anchovy':
       anchovy_sayac = anchovy_sayac + 1
       anchovyNuggetToplam = anchovyNuggetToplam + L[i].nugget
       anchovySillToplam = anchovySillToplam + L[i].sill
       anchovyRangeToplam = anchovyRangeToplam + L[i].range_
    else:
       anchovy_sayac = anchovy_sayac

sardineNuggetOrtalama = sardineNuggetToplam/sardine_sayac
sardineSillOrtalama = sardineSillToplam/sardine_sayac
sardineRangeOrtalama = sardineRangeToplam/sardine_sayac
anchovyNuggetOrtalama = anchovyNuggetToplam/anchovy_sayac
anchovySillOrtalama = anchovySillToplam/anchovy_sayac
anchovyRangeOrtalama = anchovyRangeToplam/anchovy_sayac

# print (sardineNuggetToplam,sardine_sayac,sardineNuggetOrtalama)
# print (sardineSillToplam,sardine_sayac,sardineSillOrtalama)
# print (sardineRangeToplam,sardine_sayac,sardineRangeOrtalama)
# print (anchovyNuggetToplam,anchovy_sayac,anchovyNuggetOrtalama)
# print (anchovySillToplam,anchovy_sayac,anchovySillOrtalama)
# print (anchovyRangeToplam,anchovy_sayac,anchovyRangeOrtalama)

def Gauss_Calculate(x,var,mean):
       mean = mean
       var = var
       x = x
       numerator = np.exp(- (x-mean)**2 / (2 * var))
       denominotor = np.sqrt(2* np.pi * var)
       return numerator/denominotor

def Varyance_Hesapla(x,ort):
    x = x
    ort = ort
    return (x-ort)*(x-ort)

sardineNuggetToplamVaryance=0
sardineSillToplamVaryance=0
sardineRangeToplamVaryance=0
anchovyNuggetToplamVaryance=0
anchovySillToplamVaryance=0
anchovyRangeToplamVaryance=0

for i in range(len(L)):
# print(L[i].year, L[i].nugget, L[i].sill, L[i].ranger, L[i].name)
    if(L[i].name == 'Sardine'):
       sardineNuggetToplamVaryance = sardineNuggetToplamVaryance + Varyance_Hesapla(L[i].nugget,sardineNuggetOrtalama)
       sardineSillToplamVaryance = sardineSillToplamVaryance + Varyance_Hesapla(L[i].sill,sardineSillOrtalama)
       sardineRangeToplamVaryance = sardineRangeToplamVaryance + Varyance_Hesapla(L[i].range_,sardineRangeOrtalama)
    elif L[i].name == 'Anchovy':
      anchovyNuggetToplamVaryance = anchovyNuggetToplamVaryance + Varyance_Hesapla(L[i].nugget, anchovyNuggetOrtalama)
      anchovySillToplamVaryance = anchovySillToplamVaryance + Varyance_Hesapla(L[i].sill, anchovySillOrtalama)
      anchovyRangeToplamVaryance = anchovyRangeToplamVaryance + Varyance_Hesapla(L[i].range_, anchovyRangeOrtalama)
    else:
       a=1

sardineNuggetVaryans=sardineNuggetToplamVaryance/(sardine_sayac-1)
sardineSillVaryans=sardineSillToplamVaryance/(sardine_sayac-1)
sardineRangeVaryans=sardineRangeToplamVaryance/(sardine_sayac-1)
anchovyNuggetVaryans=anchovyNuggetToplamVaryance/(anchovy_sayac-1)
anchovySillVaryans=anchovySillToplamVaryance/(anchovy_sayac-1)
anchovyRangeVaryans=anchovyRangeToplamVaryance/(anchovy_sayac-1)

sardineNuggetOlasılık = 0
sardineNuggetOlasılık = Gauss_Calculate(Nugget,sardineNuggetVaryans,sardineNuggetOrtalama)
sardineSillOlasılık = 0
sardineSillOlasılık = Gauss_Calculate(Sill,sardineSillVaryans,sardineSillOrtalama)
sardineRangeOlasılık = 0
sardineRangeOlasılık = Gauss_Calculate(Range,sardineRangeVaryans,sardineRangeOrtalama)

anchovyNuggetOlasılık = 0
anchovyNuggetOlasılık = Gauss_Calculate(Nugget,anchovyNuggetVaryans,anchovyNuggetOrtalama)
anchovySillOlasılık = 0
anchovySillOlasılık = Gauss_Calculate(Sill,anchovySillVaryans,anchovySillOrtalama)
anchovyRangeOlasılık = 0
anchovyRangeOlasılık = Gauss_Calculate(Range,anchovyRangeVaryans,anchovyRangeOrtalama)

PSardineToplamOlasılık = 0
PAnchovyToplamOlasılık = 0

PSardineToplamOlasılık = sardineNuggetOlasılık + sardineSillOlasılık + sardineRangeOlasılık
PAnchovyToplamOlasılık = anchovyNuggetOlasılık + anchovySillOlasılık + anchovyRangeOlasılık

PSardineOlasılık=0
PAnchovyolasılık=0

PSardineOlasılık = PSardineToplamOlasılık/(PSardineToplamOlasılık+PAnchovyToplamOlasılık)
PAnchovyolasılık = PAnchovyToplamOlasılık/(PSardineToplamOlasılık+PAnchovyToplamOlasılık)

if(PSardineOlasılık>PAnchovyolasılık):
    print('Sardine')
else:
    print('Anchovy')

