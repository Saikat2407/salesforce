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

// factors

public class factor {
	public static void factors(integer num)
    {
        System.debug('Factors are:');
        for(integer i= 1 ;i<=num;i++)
        {
            if(Math.mod(num, i) == 0)
            {
                System.debug(i);
            }
        }
    }
}

//power of num

public class powernum {
    public static void power(integer num, integer pow)
    {
        System.debug('Value is '+ (Math.pow(num, pow)));
    }
}

//fibonacci 

public class fibbonaci {
    public static void fibbo(integer num)
    {
        integer a,b,c;
        a=0;
        b=1;
        c=a+b;
        List<integer> series = new List<integer>{0,1};
        for(integer i=3;i<=num;i++)
        {
            series.add(c);
            a=b;
            b=c;
            c=a+b;
        }
        System.debug('Fibonnaci Siries = '+ series );
            
    }
}
				  
//max in array
				   
public class maxinarray {
    public static void showMax(){
    List<integer> arrayM = new List<integer>();
    for(integer i =0;i<=5;i++)
        {
            arrayM.add(i);
        }
        integer max = arrayM[0];
        
        for(integer i =0; i< arrayM.size() ; i++)
        {
            
                if(arrayM[i]>max)
                {
                    max = arrayM[i];
                }
        }
        
        System.debug('Max Element in array is: ' + max);

    }
}

//array in reverse order (without reverse() (using class).
	
public class reversethearray {
    public static void reverseArray(){
    List<integer> arrayM = new List<integer>();
    for(integer i =0;i<=5;i++)
        {
            arrayM.add(i);
        }
        integer startI,endI;
        startI=0;
        endI=arrayM.size()-1;
        
        
        while(startI < endI)
        {
            integer temp = arrayM[startI];
          arrayM[startI] = arrayM[endI];
          arrayM[endI] = temp;
          startI++;
          endI--;
        }
    System.debug(arrayM);

    }
}

	
//fahreneit to celcius 
	
public class temprat {
    public static Decimal fahrenheitTocelcius(Decimal fh){
        Decimal cs = (fh - 32) * 5/9;
        system.debug('@@' + cs);
        return cs.setScale(2);
    }
}
	


