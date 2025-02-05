# bandit
connection: ssh bandit2@bandit.labs.overthewire.org -p 2220

level 1: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
ls - 
cat - 

level 2: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

cat ./- 
#Si existe un archivo llamado - en el directorio actual, cat lo mostrará.

level 3:MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

cat spaces\ in\ this\ filename
\ contar espacio como parte del nombre
cat "spaces in this filename"
"tiene en cuenta todo"

level 4:2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

-rw-r----- 
#ocultar archivos

ls -a \ solo ocultos
ls -la \ detalles + ocultos

level 5: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

cd
./* tipo de archivo

level 5: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

du -b -a | grep 1033 "tamaño"
du espacio en el disco
-b bytes
-a directorios y subdirectorios
grep 

level 6:HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

-type f: Busca solo archivos regulares (excluyendo directorios, enlaces simbólicos, etc.).

-user bandit7: Filtra los archivos que pertenecen al usuario bandit7.

-group bandit6: Filtra los archivos que pertenecen al grupo bandit6.

-size 33c: Filtra los archivos que tienen un tamaño de 33 bytes (el c indica que es en bytes).

2>/dev/null: Redirige los errores (si los hay) a /dev/null, lo que significa que no se mostrarán los mensajes de error. Esto se hace para evitar que aparezcan mensajes de "permiso denegado" o errores relacionados con archivos a los que el usuario no tiene acceso.

find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

cat /var/lib/dpkg/info/bandit7.password

level 7: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

du -b data.txt 
tipo - peso
cat data.txt | grep millionth
leer archivo | filtrar palabra millionth

level 8: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

sort data.txt | uniq -u
El comando sort ordena las líneas del archivo `data.txt de manera ascendente (por defecto).
Ordenar las líneas es importante porque uniq solo puede identificar las líneas duplicadas si están adyacentes. Es por esto que primero debes ordenar el archivo.

El comando uniq se utiliza para eliminar o mostrar líneas duplicadas.
La opción -u indica que uniq debe mostrar solo las líneas que son únicas, es decir, aquellas que no tienen duplicados en el archivo (después de que han sido ordenadas por sort).

level 9: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

strings data.txt | grep ===
busca "==="
