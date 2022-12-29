# - “Hola mundo!”-
print(3 / 2)
1.5 

peso = input("¿Cuál es tu peso en kg? ")
estatura = input("¿Cuál es tu estatura en metros?")
imc = round(float(peso)/float(estatura)**2,2)
print("Tu índice de masa corporal es " + str(imc))

Tu índice de masa corporal es 24.22

class Vehiculo():
    counter = 0
    color = ""
    ruedas = 0
    def __init__(self, color, ruedas):
        self.color=color
        self.ruedas=ruedas  
        
           

class Coche(Vehiculo): 
    velocidad = 0
    cilindrada = 0
    def __init__(self, color, ruedas, velocidad, cilindrada):
        super().__init__(color, ruedas)
        self.velocidad = velocidad
        self.cilindrada = cilindrada

    
class Bicicleta(Vehiculo): 
    tipo = ""
    def __init__(self, color, ruedas, tipo):
        super().__init__(color, ruedas)
        self.tipo = tipo
      
        
class Camioneta(Coche):
    carga = 0
    def __init__(self, color, ruedas, velocidad, cilindrada, carga):
        super().__init__(color, ruedas, velocidad, cilindrada)
        self.carga = carga
        


class Motocicleta(Bicicleta): 
    velocidad = 0
    cilindrada = 0
    def __init__(self,color, ruedas, tipo, velocidad, cilindrada):
        super().__init__(color, ruedas,tipo)
        self.velocidad = velocidad
        self.cilindrada = cilindrada
        
        
a = Camioneta("marron",8, 120, 400, 500)
b = Coche("verde",4, 120, 800)
c = Bicicleta("azul",2,"triciclo")
d = Coche("verde",4, 120, 800)
e = Motocicleta("azul",2,"triciclo",150, 200)
lista_vehiculos = [a.__dict__,b.__dict__,c.__dict__,d.__dict__,e.__dict__]
print(lista_vehiculos)
