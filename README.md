# salesforce

apex prog to check the num is prime or not 

public class prime {
	public static void getPrime(){
		integer x = 0;
    	for(x=0;x<10;x++)
    	{
        integer count=0;
		integer y =0;
        for( y=x; y>=1;y--)
        {
            if(math.mod(x,y)==0 )
            {
                count++;
            }
        }
        if(count==2 || count==1){
            system.debug('this is prime');
        }
        else{
            system.debug('This is not prime number ');      
        }
    	}
  }
}
