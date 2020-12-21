# Konversi-Suhu
public class KonversiWaktu {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        System.out.println("Pilihan Konversi:\n" + "1. jam -> Menit\n" + " 2. Detik -> Hari, Jam, Menit, dan detik");
        System.out.println("\nMasukkan pilihan");
        try (Scanner options = new Scanner(System.in)) {
            if (!options.hasNextInt()) {
                System.out.println("Itu Alfabet, Anda salah!");
            } else {
                if (options.nextInt() == 1) {
                    System.out.println("Masukkan jam :");
                    Scanner hours = new Scanner(System.in);
                    JamKeMenit(hours.nextInt());
                } else {
                    System.out.println("Masukkan detik :");
                    try (Scanner seconds = new Scanner(System.in)) {
                        detikKeHari(seconds.nextLong());
                    }
                }
            }
        }
    }
    
    
    
    public class JamKeMenit {
    public static void main(String[] args) {
        int jam = 20;
        long menit = jam * 60;
        System.out.println("Menit: " + menit);
    }
}




public class detikKeHari {
    public static void main(String[] args) {
        int detik = 0;
        //hari
        int hari = (int) (detik / (60 * 60 * 24));
        
        //jam
        detik %= (60 * 60 * 24);
        int jam = (int) (detik / (60 * 60));
        
        //menit
        detik %= (60 * 60);
        int menit = (int) (detik / 60);
        
        //detik
        detik %= 60;
        
        System.out.println(hari + " Hari, " + jam + "jam, " +menit + "menit, " + detik + " detik");
    }
}
