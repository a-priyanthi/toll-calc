import java.util.Scanner;
abstract class vehicle
{
    final int num; static int count; //static int c=0;
    static final int m; static int reg[]=new int[10];

    static{m=50;}
    vehicle(int num)
    {
        this.num=num;
    }

    static void count()
    {
        count++;
    }

    abstract int calc();

    void display()
    {
        System.out.println("Vehicle number: "+num);
        System.out.println("Toll amount: $"+calc());
        
    }


}

class car extends vehicle
{
    //int toll;
    car(int num)
    {
        super(num);
        reg[count]=num;
    }

    int calc()
    {
        int toll = 200+m;
        return toll;
    }

    

    /*void display()
    {
        System.out.println("Vehicle number: "+num);
        System.out.println("Toll amount: $"+calc());
        
    }*/
}

class bus extends vehicle
{
    //int toll;
    bus(int num)
    {
        super(num);reg[count]=num;
    }

    int calc()
    {
        int toll = 300+m;
        return toll;
    }


    /*void display()
    {
        System.out.println("Vehicle number: "+num);
        System.out.println("Toll amount: $"+calc());
        
    }*/
}

class truck extends vehicle
{
    //int toll;
    truck(int num)
    {
        super(num);reg[count]=num;
    }

    int calc()
    {
        int toll = 400+m;
        return toll;
    }

    
    /*void display()
    {
        System.out.println("Vehicle number: "+num);
        System.out.println("Toll amount: $"+calc());
        
    }*/
}

public class vtc
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int ch; int i=0;int j=0;int k=0;

        car c[]=new car[10];
        bus b[]=new bus[10];
        truck t[]=new truck[10];
        
        do
        {
            System.out.println();
            System.out.println("VEHICLE TOLL CALCULATION -----------------------\n1.Car\n2.Bus\n3.Truck\n4.Count\n5.Exit");
            System.out.println();
            System.out.println("Enter Choice: ");
            ch=s.nextInt();

            switch(ch)
            {
                case 1:
                    System.out.print("Enter vehicle number: ");
                    int n1=s.nextInt();

                    c[i]=new car(n1);c[i].display();c[i].count();

                    i++;
                    break;

                case 2:
                    System.out.print("Enter vehicle number: ");
                    int n2=s.nextInt();

                    b[j]=new bus(n2);b[j].display();b[j].count();

                    j++;
                    break;

                case 3:
                    System.out.print("Enter vehicle number: ");
                    int n3=s.nextInt();

                    t[k]=new truck(n3);t[k].display();t[k].count();

                    k++;
                    break;

                case 4:
                    System.out.println("Vehicle Count: "+vehicle.count);
                    //System.out.println("Vehicle Numbers: "+);
                    for(int x=0;x<vehicle.count;x++)
                    {
                        System.out.println("Vehicle number:"+vehicle.reg[x]);
                    }
                    break;

                case 5:
                    return;
                
                default:
                    System.out.println("Invalid Choice");
                    break;
            }
        }while(ch!=5);
    }
}
