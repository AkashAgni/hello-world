# hello-world
This is Akash's repository.


//The following is a prime number finder program in Java (eclipse IDE). 

public class PrimeFinder {
	public static void main(String[] args) {
		
		double p = 5;
		double c = 0;
		double n = 100000; //This represents the nth prime you want to find. 
                       //For instance, if you want to find the 100th prime, set n=100; 
		
		while(c < (n-2)) {
		double k = 0;	
		for(double i = 2; i <= (p/2); ++i) {	
			if((p%i)==0) {
				++k;
				i = (p/2); //Terminate the loop.
			}
		}
			if (k >= 1) {
				p = p+2;
			}
			else {
				System.out.println(p);
				p = p+2;
				++c;
			}		
		}			
	}
}
