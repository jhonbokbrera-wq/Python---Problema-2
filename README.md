# Python---Fase 5 - Evaluación Final POA

Solución del Problema #2 del banco de problemas de la Fase 5

print("")
print(" -----RESTAURANTE - PRECIOS----- ")
print("")

print("-----MENU PRINCIPAL-----")
print("Sopa del Dia:                        $2.000")
print("Ensalada Cesar:                      $3.000")
print("Pasta Carbonara:                     $5.000")
print("(Plato Principal)Pollo a la Parilla: $6.000")
print("Postre del Dia:                      $4.000")
print("")
print("-----BEBIDAS-----")
print("Agua MIneral:                        $1.000")
print("Refresco Natural:                    $2.000")
print("Cerveza Artezanal:                   $3.000")
print("VIno de la Casa:                     $4.000")
print("Cafe Expreso:                        $2.000")
print("")
print("-----PROMOCIONES-----")
print("Combo Almuerzo: Sopa + Plato Principal + Refresco Natural + Postre: $14.000")
print("Combo Cena: Plato Principal + Refresco Natural + Postre:            $12.000")
print("Combo Familiar: 4 Platos Principales + 4 Refrescos Naturales:       $32.000")
print("")
print("-----------------------------------------------------------")
print("¡Disfruta de nuestra deliciosa comida a precios accesibles!")
print("-----------------------------------------------------------")


print(""    )


menu = [
    ["Sopa del Dia", "Menu Principal", 2000],
    ["Ensalada Cesar", "Menu Principal", 3000],
    ["Pasta Carbonara", "Menu Principal", 5000],
    ["Pollo a la Parrilla", "Menu Principal", 6000],
    ["Postre del Dia", "Menu Principal", 4000],

    ["Agua Mineral", "Bebida", 1000],
    ["Refresco Natural", "Bebida", 2000],
    ["Cerveza Artesanal", "Bebida", 3000],
    ["Vino de la Casa", "Bebida", 4000],
    ["Cafe Expreso", "Bebida", 2000],

    ["Combo Almuerzo", "Promocion", 14000],
    ["Combo Cena", "Promocion", 12000],
    ["Combo Familiar", "Promocion", 32000]
]


categoria_objetivo = "Promocion"

print(f"PRODUCTOS EN LA CATEGORIA OBJETIVOS '{categoria_objetivo}' CON 15% DE DESCUENTO:")
print("")
for producto in menu:
    nombre = producto[0]
    categoria = producto[1]
    precio = producto[2]
    if categoria == categoria_objetivo:
        descuento = precio * 0.15
        precio_con_descuento = precio - descuento
        print(f"{nombre}: Precio Original: ${precio}, Precio con Descuento: ${precio_con_descuento}")
        
print("")

print(f"PRODUCTOS MAYOR A UN UMBRAL QUE APLICAN 15% DE DESCUENTO:")   
print("")     

umbral_definido = 4000    

for producto in menu:
    nombre = producto[0]
    precio = producto[2]
    if precio > umbral_definido:
        descuento_extra = precio * 0.15
        precio_con_descuento = precio - descuento_extra
        print(f"{nombre}: Precio Original: ${precio}, Precio con Descuento: ${precio_con_descuento}")
    else:
        print(f"{nombre}: Precio Original: ${precio}, No Aplica Descuento")
        
print("")
