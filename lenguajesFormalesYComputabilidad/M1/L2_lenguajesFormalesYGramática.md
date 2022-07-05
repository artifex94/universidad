# Lenguajes formales y gramáticas

## *Gramáticas formales*
Una gramática formal es una descripción estructurada de las sentencias de un lenguaje. Una gramática formal que permite especificar, de manera finita, el conjunto de cadenas de símmbolos que constituyen un lenguaje. Este lenguaje se especifica mediante un *alfabeto*; un simbolo inicial llamado *axioma*; un conjunto de símbolos especiales denominados símbolos no terminales, que permiten obtener subcunjuntos del lenguaje y estados intermedios de la generación de palabreas; y un conjunto de reglas que permiten realizar las transformaciones desde los símbolos no terminales a las palabras del lenguaje.

Una gramática formal $G$ se define como una cuádrupla:

$G=(\Sigma T, \Sigma N, S, P)$

en la cual

$\Sigma T=$ {conjunto finito de símbolos terminales}

$\Sigma N=$ {Conjunto finito de símbolos no terminales}

$S=$ símbolo inicial llamado axioma pertenece a $\Sigma N$

$P=$ {conjunto de producciones o de reglas de derivación}

Todas las cadenas del lenguaje definido por la gramática están formadas con símbolos del alfabeto de los terminales $\Sigma T$. El alfabeto de símbolos terminales $\Sigma T$ se define por enumeración.

El alfabeto de símbolos no terminales $\Sigma N$ es el conjunto de símbolos introducidos como elementos auxiliares para la definición de la gramática y que no figuran en las sentencias del lenguaje. se define por enimeración de sus símbolos no terminales.

La intersección entre el alfabeto de los símbolos terminales y el alfabeto de los símbolos no terminales es el conjunto vacío: $\{\Sigma N\} \cap \{\Sigma T\} = \{\empty\}$.

El conjunto de producciones $P$ representa cómo se realiza la transformación desde los símbolos no terminales a las palabras del lenguaje, por lo tanto, una producción es una regla de definición. Cada producción es un par $(\alpha, \beta)$ que se representa como $\alpha \to  \beta$, donde $\alpha$ y $\beta$ son cadenas y la expresión $\to$ significa que $\alpha$ debe ser sustituida por $\beta$ al momentode aplicar la prdocción.

## *Definiciones*

### *Derivación:*
Es un proceso que permite obtener las palabreas del lenguaje partiendo del axioma y aplicando las reglas de producción por la parte izquierda de esta.

La palabra quedará definitivamente formada cuando esté compuesta sólo por símbolos terminales.

### *Forma sentencial:*
Se dice que $x$ es una forma setencial si existe una derivación, o secuencia de derivaciones, que, partiendo del axioma $S$, permite obtener $x$:

$S \to x$

### *Sentencia:*
$x$ es una sentencia, si $x$ es una forma sentencial y todos sus símbolos pertenecen al alfabeto de los símbolos terminales $\Sigma T$:

$S \to x$, y $x \in \Sigma T$