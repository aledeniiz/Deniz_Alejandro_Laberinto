https://github.com/aledeniiz/Deniz_Alejandro_Laberinto
# Deniz_Alejandro_Laberinto
def construir_laberinto(muro):
    
    filas, columnas = 5, 5

    
    laberinto = [[' ' for _ in range(columnas)] for _ in range(filas)]

    # Colocar muros en el laberinto
    for coordenada in muro:
        fila, columna = coordenada
        laberinto[fila][columna] = 'X'

    
    laberinto[4][4] = 'S'

    return laberinto


muro = ((0,1), (0,2), (0,3), (0,4), (1,1), (2,1), (2,3), (3,3), (4,0), (4,1), (4,2), (4,3))


laberinto = construir_laberinto(muro)


for fila in laberinto:
    print(' '.join(fila))
