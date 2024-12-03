En [Visual Studio Code](https://code.visualstudio.com/) con la extensión de [LaTex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop). 

Para que la extensión compile desde un archivo específico se le debe modificar el comentario en el archivo "archivoRoot.tex"
%!TeX root = Guias/CompiladorGuias.tex
Se pone la dirección del archivo a compilar.

Si hay errores, lo más seguro es que sean las direcciones de imágenes y otros archivos que se referencia en un .tex. 

**Por ejemplo:** Se esta compilando el archivo %!TeX root = Cortos/CompiladorCortos.tex y S1C1 necesita una imagen del folder Imagenes. El error se vera en 
```
\includegraphics[width=0.3\textwidth]{Imagenes/IMG1/venn.png}
```

Esto es por el folder Imagenes no esta dentro del folder Cortos, que es donde esta S1C1.tex.

El arreglo es:
```
\includegraphics[width=0.3\textwidth]{../Imagenes/IMG1/venn.png}
```

El .. regresa en la jerarquía de folders y ahí encuentra el folder Imagenes.


