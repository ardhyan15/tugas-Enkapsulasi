# tugas-Enkapsulasi

public class Main {
    public static void main(String[] args) {

        // Buatlah dua buah objek dari class Person
        Person personAnton = new Person();
        personAnton.setNama("Anton");
        personAnton.setJenisKelamin('L');
        personAnton.setUmur(25);

        System.out.println(personAnton.getNama() + ", Jenis Kelamin: " + personAnton.getJenisKelamin() +
                ", Umur: " + personAnton.getUmur());

        // Objek kedua
        Person personRiko = new Person();
        personRiko.setNama("Riko");
        personRiko.setJenisKelamin('P');
        personRiko.setUmur(30);

        System.out.println("\n" + personRiko.getNama() + ", Jenis Kelamin: " +
                personRiko.getJenisKelamin() + ", Umur: " + personRiko.getUmur());
    }
}

class Person{
    private String nama;
    private char jenisKelamin;
    private int umur;

    // Setter method for attributes
    public void setNama(String nama){
        this.nama=nama;
    }

    public void setJenisKelamin(char jenisKelamin){
        if(jenisKelamin == 'L' || jenisKelamin=='P'){
            this.jenisKelamin=jenisKelamin;
        } else{
            throw new IllegalArgumentException("Invalid gender value.");
        }
    }

    public void setUmur(int umur){
        if(umur >=18 && umur <=100){
            this.umur=umur;
        }else{
            throw new IllegalArgumentException("Age must be between 18 and 100 years old.");
        }
    }

    // Getter methods for attributes
    public String getNama(){
        return nama;
    }

    public char getJenisKelamin(){
        return jenisKelamin;
    }

    public int getUmur(){
        return umur;
    }
}
