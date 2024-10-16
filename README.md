# Latihan 1

# Buatlah kode program java untuk:
• Mendeklarasikan class Person, dengan
atribut Nama, JenisKelamin, Umur dan
lengkapi dengan access modifier.
• Buatlah dua buah objek dari class Person
bernama Anton dan Riko dan panggil
method setter dan getter.











class Person {
    // Atribut private
    private String nama;
    private String jenisKelamin;
    private int umur;

    // Constructor untuk inisialisasi Person
    public Person(String nama, String jenisKelamin, int umur) {
        this.nama = nama;
        this.jenisKelamin = jenisKelamin;
        this.umur = umur;
    }

    // Setter dan Getter untuk atribut nama
    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getNama() {
        return this.nama;
    }

    // Setter dan Getter untuk atribut jenisKelamin
    public void setJenisKelamin(String jenisKelamin) {
        this.jenisKelamin = jenisKelamin;
    }

    public String getJenisKelamin() {
        return this.jenisKelamin;
    }

    // Setter dan Getter untuk atribut umur
    public void setUmur(int umur) {
        this.umur = umur;
    }

    public int getUmur() {
        return this.umur;
    }
}

public class Main {
    public static void main(String[] args) {
        // Membuat objek Anton dan Riko
        Person anton = new Person("Anton", "Laki-laki", 25);
        Person riko = new Person("Riko", "Laki-laki", 30);

        // Menampilkan informasi awal Anton dan Riko
        System.out.println("Data Anton:");
        System.out.println("Nama: " + anton.getNama());
        System.out.println("Jenis Kelamin: " + anton.getJenisKelamin());
        System.out.println("Umur: " + anton.getUmur());

        System.out.println("\nData Riko:");
        System.out.println("Nama: " + riko.getNama());
        System.out.println("Jenis Kelamin: " + riko.getJenisKelamin());
        System.out.println("Umur: " + riko.getUmur());

        // Mengubah data Anton dan Riko menggunakan setter
        anton.setNama("Anton Pratama");
        anton.setUmur(26);
        riko.setNama("Riko Wijaya");
        riko.setUmur(31);

        // Menampilkan data setelah diubah
        System.out.println("\nData Anton setelah diubah:");
        System.out.println("Nama: " + anton.getNama());
        System.out.println("Umur: " + anton.getUmur());

        System.out.println("\nData Riko setelah diubah:");
        System.out.println("Nama: " + riko.getNama());
        System.out.println("Umur: " + riko.getUmur());
    }
}
