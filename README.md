# hello-world
This is Akash's repository.


//The following is a prime number finder program in Java (eclipse IDE). 


	public class PrimeFinder {
		public static void main(String[] args) {
		
		double p = 5;	   //This is the number that is being checked to see if it is a prime. Starting at p = 5 so 
				   //that it does not mess up the for loop conditions.
		double c = 0; 	   //This double holds the order of the prime. Eg, if the 134th prime is found, c will equal 134.
		double n = 100000; //This represents the nth prime you want to find. 
                       		   //For instance, if you want to find the 100th prime, set n=100; 
		
		while(c < (n-2)) {
		double factors = 0;	
		for(double i = 2; i <= (p/2); ++i) {	
			if((p%i)==0) {
				++factors;
				i = (p/2); //Terminate the loop. This significantly shortens the processing time. Without this 
					   //line, finding the prime at n = 100,000 takes 1 hour instead of (under) 10 mins. 
			}
		}
		
		//If p is not prime, the 2 will be added to p (there is no need to check an even number and p is always odd).
		//If p is prime, then it will be printed and 1 will be added to c. Of course, you don't need to print all 
		//the prime numbers leading up to the one you want, but I thought it would be nice to see it all go.  
			if (factors >= 1) {
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
