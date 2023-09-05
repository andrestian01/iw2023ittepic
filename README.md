# iw2023ittepic
 
1.- Crear una rama v0.2.
git branch v0.2

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/4ac4ea40-389e-4713-8f79-ee2583387424)

2.- Posiciona tu carpeta de trabajo en esta rama.
git checkout v0.2

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/eb4baf0e-6a30-45bf-bec6-ddf589bb19ca)

---------------------------------------------------------------------------------------------------------------------
# Añadir fichero 1.txt
1.- Añadir un fichero 2.txt en la rama v0.2.
touch 2.txt
git add .
git commit -m "añadido 2.txt"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/8e433ac8-3db0-4136-979d-6638df5a5364)

-------------------------------------------------------------------------------------------------------------------------
# Crear rama remota v0.2
1.	Subir los cambios al repositorio remoto
git push origin v0.2

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/0c78ecc8-4317-4964-b3d0-c0d1a6163584)

------------------------------------------------------------------------------------------------------------------------

# Merge directo
1.	Posicionarse en la rama master
git checkout master

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/ba23b03e-b819-4352-bd9e-2db3bec763e3)

3.	Hacer un merge de la rama v0.2 en la rama master
git merge v0.2 -m "merge v0.2 sin conflictos"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/e7d560c1-ec65-4231-b697-8c544d4065db)

----------------------------------------------------------------------------------------------------------------------

# Merge con conflicto
1.	En la rama master poner Hola en el archivo 1.txt y hacer commit
git checkout master
echo "Hola" >> 1.txt
git add .
git commit -m "hola en 1.txt"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/83cb057d-4ca1-411b-b341-d5d9a0fe7419)


2.	Posicionarse en la rama v0.2 y poner Adiós en el archivo 1.txt y hacer commit
git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/7a7d42d6-3f34-4cbf-a042-26cd7efc03fc)


3.	Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
git checkout master
git merge v0.2
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/13bc3e8b-bc65-454b-93eb-895fedaebcae)

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/b27e0f05-a27e-40d0-8764-275062749040)



4.	Listar las ramas con merge y las ramas sin merge
git branch --merged

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/1600d6c4-d03f-4073-9292-76ba6a44a74b)

git branch --no-merged

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/d96da955-fc08-4e5f-abb9-52b50a7e7b17)


5.	Arreglar conflicto anterior y hacer un commit
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"

![image](https://github.com/andrestian01/iw2023ittepic/assets/68936076/44127d0e-7a19-4bca-8c38-e9b479621adb)

----------------------------------------------------------------------------------------------------------------------------
Borrar rama
