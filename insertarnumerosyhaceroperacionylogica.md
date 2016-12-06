import java.util.Scanner;
public class alfa {
	static int  x,y,z;
	static int w,u,l;
	
	public double factorial(int n){
		 if (n==0)
		        return 1;
		    else
		        return n*(factorial(n-1));
		   
		}
	public void paroimpar(int n){
		if(n%2==0){
			System.out.println("es par");
			}else {
				System.out.println("es impar");
			}
	}
	public void mayoromenor(){
		if(x<y&& y<z&&z<w&&w<u&&u<l){
			System.out.println("el mayor es: "+l);
			}
		if(x<y&&y>z&&w<y&&u<y&&l<y){
				System.out.println("el mayor es :"+y);
		}
		if(y<x&&x>z&&l<x&&u<x&&w<x){
			System.out.println("el mayor es :"+x);
	}if(x<z&&y<z&&w<z&&u<z&&l<z){
		System.out.println("el mayor es:"+z);
	}
	if(x<u&&y<u&&w<u&&z<u&&l<u){
		System.out.println("el mayor es:"+u);
	
		
	}
	if(x<w&&y<w&&u<w&&z<w&&l<w){
		System.out.println("el mayor es:"+w);
	
	
	}
	}
	public void suma(){
		int suma=0;
		suma=x+y+z+w+u+l;
		System.out.println(suma);
	}
	
	public static void main(String[] args) {
		 Scanner sc= new Scanner ( System.in);
		 
		 System.out.println("inserta el numero matematico a elegir");
		 x=sc.nextInt();
		 System.out.println("inserta el numero matematico a elegir");
		 y=sc.nextInt();
		 System.out.println("inserta el numero matematico a elegir");
		 z=sc.nextInt();
		 System.out.println("inserta el numero matematico a elegir");
		 w=sc.nextInt();
		 System.out.println("inserta el numero matematico a elegir");
		 u=sc.nextInt();
		 System.out.println("inserta el numero matematico a elegir");
		 l=sc.nextInt();
		 cola cola1=new cola();
	        cola1.insertar(x);
	        cola1.insertar(y);
	        cola1.insertar(z);
	        cola1.insertar(w);
	        cola1.insertar(u);
	        cola1.insertar(l);
	        cola1.imprimir();
		    alfa beta=new alfa();
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(x));
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(y));
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(z));
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(w));
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(u));
	        System.out.println("factorial del numero");
	        System.out.println(beta.factorial(l));
	        System.out.println("*****************************************************************************");
	       beta.mayoromenor();
	       System.out.println("*******************************************************************************");
	       System.out.println(+x+" es:");
	       beta.paroimpar(x);
	       System.out.println(+y+" es:");
	       beta.paroimpar(y);
	       System.out.println(+z+" es:");
	       beta.paroimpar(z);
	       System.out.println(+w+" es:");
	       beta.paroimpar(w);
	       System.out.println(+u+" es:");
	       beta.paroimpar(u);
	       System.out.println(+l+" es:");
	       beta.paroimpar(l);
	       System.out.println("*******************************************************************************");
	       System.out.println("La suma es:");
	       beta.suma();
	       listatipopila pila1=new listatipopila();
	       
	       int ty=cola1.extraer();
	       int to=cola1.extraer();
	       int ta=cola1.extraer();
	       int tu=cola1.extraer();
	       int e=cola1.extraer();
	       int o=cola1.extraer();
	       
	       pila1.insertar(ty);
	       pila1.insertar(to);
	       pila1.insertar(ta);
	       pila1.insertar(tu);
	       pila1.insertar(e);
	       pila1.insertar(o);
	        pila1.imprimir();
	       
	       
	       
	       
	       
	       
		
	}

}

public class nodo {
	//atributos de la clase nodo
		Object dato; 
		nodo Sig;
		//constructor del nodo para crear un objeto
		public nodo(Object Valor){
			dato=Valor;
			Sig=null;
		}
		//Constructor del nodo para crear un objeto del siguiente nodo
		public nodo(Object Valor,nodo Sign){
			dato=Valor;
			Sig=Sign;
		}

}
public class cola {
	  class Nodo {
	        int info;
	        Nodo sig;
	    }
	    
	    private Nodo raiz,fondo;
	    
	    cola() {
	        raiz=null;
	        fondo=null;
	    }
	    
	    boolean vacia (){
	        if (raiz == null)
	            return true;
	        else
	            return false;
	    }

	    void insertar (int info)
	    {
	        Nodo nuevo;
	        nuevo = new Nodo ();
	        nuevo.info = info;
	        nuevo.sig = null;
	        if (vacia ()) {
	            raiz = nuevo;
	            fondo = nuevo;
	        } else {
	            fondo.sig = nuevo;
	            fondo = nuevo;
	        }
	    }

	    int extraer ()
	    {
	        if (!vacia ())
	        {
	            int informacion = raiz.info;
	            if (raiz == fondo){
	                raiz = null;
	                fondo = null;
	            } else {
	                raiz = raiz.sig;
	            }
	            return informacion;
	        } else
	            return Integer.MAX_VALUE;
	    }

	    public void imprimir() {
	        Nodo reco=raiz;
	        System.out.println("Listado de todos los elementos de la cola.");
	        while (reco!=null) {
	            System.out.print(reco.info+"\n");
	            reco=reco.sig;
	        }
	        System.out.println();
	    }
	        

}
public class listatipopila {
	class Nodo{
        int info;
        Nodo sig;
        }
    private Nodo raiz;
    
    listatipopila(){
        raiz=null;
        
    }
    public void insertar(int x){
        Nodo nuevo;
        nuevo=new Nodo();
        nuevo.info=x;
        if(raiz==null)
        {
            nuevo.sig=null;
            raiz=nuevo;
        }
        else
        {
            nuevo.sig=raiz;
            raiz=nuevo;
        }
    }
    public int extraer(){
        
        if(raiz!=null){
            int informacion=raiz.info;
            raiz=raiz.sig;
            return informacion;
        }
        else
        {
        return Integer.MAX_VALUE;    
        }
       }
    public void imprimir(){
        Nodo reco=raiz;
        System.out.println("Lista de todos los elementos de la pila");
        while(reco!=null){
            System.out.println(reco.info+"");
            reco=reco.sig;
        }
        System.out.println();
    }
    public boolean vacia(){
        if(raiz==null){
            return true;
        }else{
            return false;
        }
    }
    public int cantidad(){
        int cant=0;
        Nodo reco=raiz;
        while(reco!=null){
            cant++;
            reco=reco.sig;
        }
        return cant;
      }

}







