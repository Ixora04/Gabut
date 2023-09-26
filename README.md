import java.util.Scanner;
public class Gabut {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
       int jumlahSaldo=(1000000);
        
        System.out.println("Selamat datang di Bank");
        System.out.println();
        System.out.println("Saldo rekening Anda : Rp." + jumlahSaldo);
        System.out.println("Apakah Anda inggin melakukan \"penyetoran\" atau \"penarikan\"?");
        System.out.println("Ketik \"batal\" untuk membatalkan.");
        System.out.println();
        
        String transaksi = input.nextLine();
        switch(transaksi){
            case "penyetoran":
                System.out.println();
                System.out.print("Silahkan masukan nominal setoran Anda : Rp."); int setoran = input.nextInt();
                System.out.println();
                System.out.println("Penyetoran berhasil.");
                System.out.println("Saldo Anda saat ini : Rp." + (jumlahSaldo + setoran));
                
                break;
        
            case "penarikan":
                System.out.println();
                System.out.print("Silahkan masukan nominal penarikan Anda : Rp."); int tarikan = input.nextInt();
                System.out.println();
                if (tarikan <= jumlahSaldo){
                    System.out.println("Penarikan berhasil.");
                    System.out.println("Saldo Anda saat ini : Rp." + (jumlahSaldo - tarikan));
                } else {
                    System.out.println("Maaf, jumlah saldo Anda tidak mencukupi.");
                }
                break;
        
            case "batal":
                System.out.println("Terimakasih, silahkan datang kembali.");
                
                break;
                
            default:
                System.out.println("Silahkan periksa kembali input yang Anda masukan!");
        }

        input.close();
    }
    
}
