# repositorio2
los 7 numeros impares



public class MyClass {
    public static void main(String args[]) {
      int x=1;
      int y=3;
      int o=5;
      int p=7;
      int r=9;
      int d=11;
      int c=13;
      int z=x+y+o+p+r+d+c;

      System.out.println("Sum of x+y+o+p+r+d+c = " + z);
    }
}


public class Impares {
    int n;
    int[] arr ;

    Impares(int n){
        this.n = n;
        arr = new int[n];
        getImpar();
    }

    private void getImpar(){
        int counter = 1;
        int i = 0;
        while(i < n){
            if(counter % 2 != 0){
                arr[i] = counter;
                i++;
            }
            counter++;
        }
    }
    private int getSum(){
        int sum =0;
        for(int s: arr){
            sum += s;
        }
        return sum;
    }

    public String toString(){
        String res = "";
        for(int n: arr){
            if(n == arr[arr.length -1]){
                res += n ;
            }else{
                res += n + " + ";
            }
        }
        res += " = " + getSum();
        return res;
    }

    public static void main(String[] args) {
        System.out.println(ingrese un nuero());
        Scanner input = new Scanner(System.in);
        int n = input.nextInt();
        Impares impares = new Impares(n);
        System.out.println(impares.toString());
    }
}
