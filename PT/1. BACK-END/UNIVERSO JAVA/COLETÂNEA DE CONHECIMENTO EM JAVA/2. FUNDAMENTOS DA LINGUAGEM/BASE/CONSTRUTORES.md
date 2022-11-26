### **Sobre os "Construtores"**
Os **"construtores"** são responsáveis por criar objetos em memória.

##### <br>

### **Características dos "Construtores"**
* Possuem como principal função a inicialização dos dados.
* Seus nomes devem ser idênticos aos das **"classes"** as quais pertencem.
* Não possuem, sob nenhuma hipótese, **"returns"**.
* Se um **"construtor"** não for declarado em uma determinada **"classe"**, automaticamente, por padrão, haverá um **"construtor default"** acoplado a ela.
* A presença de mais de um **"construtor"** numa mesma **"classe"** é categorizada como **"sobrecarga"**.
* O Java diferencia os **"construtores"** por meio da quantidade de **"parâmetros"**.
 
##### <br>

### **Em que momento são executados?**
Durante a execução de uma **"instanciação de um objeto"**.

##### <br>

### **Quais são seus usos mais comuns?**
* Iniciam os valores dos **"atributos"**.
* Permitem ou obrigam que um determinado **"objeto"** receba dados ou dependências no momento de sua **"instanciação"** ao passo que **"injetam dependências"**. 

##### <br>

### **Exemplos de uso quanto aos "Construtores"**
~~~ java

public class Product {
	public String name;
	public double price;
	public int quantity;

	// CONSTRUTOR DEFAULT
	Product(){
	}    
  
	// CONSTRUTOR
	Product(String name, double price){
    	this.name = name;
     	this.price = price;
	}   
   
	// SOBRECARGA DE CONSTRUTOR
	Product(String name, double price, int quantity){
     	this.name = name;
     	this.price = price;
     	this.quantity =  quantity;
 	} 
    
	// REUSANDO UM CONSTRUTOR DENTRO DE OUTRO
	Product(String name, double price, int quantity){
     	this(nome);
     	this.price = price;
     	this.quantity =  quantity;
 	} 
 
	...
    
	public double totalValueInStock() {
	return price * quantity;
	}
    
	public void addProducts(int quantity) {
	this.quantity += quantity;
	}
    
	public void removeProducts(int quantity) {
	this.quantity -= quantity;
	}
    
	public String toString() {
	return name
	+ ", $ "
	+ String.format("%.2f", price)
	+ ", "
	+ quantity
	+ " units, Total: $ "
	+ String.format("%.2f", totalValueInStock())
	}
}

~~~

~~~ java

public class Program {
public static void main(String[] args) {
	Locale.setDefault(Locale.US);
	Scanner sc = new Scanner(System.in);

    	System.out.println("Enter product data: ");
	System.out.print("Name: ");
	product.name = sc.nextLine();
    
	System.out.print("Price: ");
	product.price = sc.nextDouble();
	
   	System.out.print("Quantity in stock: ");
	product.quantity = sc.nextInt();
    
     	// A KEYWORD "NEW" CHAMA O CONSTRUTOR DA CLASSE "PESSOA" E CONSTRÓI O OBJETO.
   	Product product = new Product(name, price, quantity);
    
	System.out.println();
	System.out.println("Product data: " + product);
	System.out.println();
     
	System.out.print("Enter the number of products to be added in stock: ");
	quantity = sc.nextInt();
	product.addProducts(quantity);
    
	System.out.println();
	System.out.println("Updated data: " + product);
	System.out.println();
    
	System.out.print("Enter the number of products to be removed from stock: ");
	quantity = sc.nextInt();
	product.removeProducts(quantity);
    
	System.out.println();
	System.out.println("Updated data: " + product);
	sc.close();
	}
}

~~~
