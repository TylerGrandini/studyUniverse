### **Sobre a "Classe Object"**
Toda e qualquer classe é uma subclasse da superclasse **"Object"**, mesmo quando "extends Object" está em desuso. Ou seja, o java faz com que as classes herdem os métodos, automaticamente, da classe **"Object"**.

<br>

### **Métodos da "Classe Object"**
**toString()** 
<br>
Retorna um texto conciso e informativo sobre os objetos de sua classe.

**getClass()** 
<br>
Quando em uma classe existem vários tipos de objetos, onde um herda do outro, o método **"getClass()"** retornará o nome do objeto atual e não de sua superclasse.

**clone()** 
<br>
Retorna uma referência ou uma cópia do objeto.

**equals(Object obj)** 
<br>
Faz comparações entre dois objetos. Retorna **"true"** se os objetos forem os mesmos ou **"false"** se não forem. É útil para saber se dois objetos apontam para o mesmo local na memória.
 

**hashCode()** 
<br>
Retorna um inteiro único de cada objeto.

**notify()** 

**notifyAll()**

**wait()**


https://www.alura.com.br/apostila-csharp-orientacao-objetos/classe-object