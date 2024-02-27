import java.util.HashMap;
import java.util.HashSet;
class Metin {
    String karakter;
    int sayi;

    public Metin(String karakter, int sayi) {
        this.karakter = karakter;
        this.sayi = sayi;

    }
}

public class odev6 {
    public static void main(String[] args) {
        HashMap<Integer, Metin> metinMap =new HashMap<>();

        metinMap.put(1,new Metin("yalniz ben bilirim",123456));
        metinMap.put(2,new Metin("hiç kimse bilmez",7890));
        metinMap.put(3,new Metin("bazıları bilir, bazıları bilmez", -123));

        Metin Yalniz = metinMap.get(3);
        System.out.println( Yalniz.karakter + ", " + Yalniz.sayi );

        for (int numara : metinMap.keySet()){
            Metin metin= metinMap.get(numara);
            System.out.println(numara + " -> " + metin.karakter + ", " + metin.sayi + " yaşında.");

            HashSet<Character> uniqueCharacterSet = findUniqueCharacters(metin.karakter);
            System.out.println("Benzersiz karakter kümesi: " + uniqueCharacterSet);
        }

    }
    public static HashSet<Character> findUniqueCharacters(String text) {
        HashSet<Character> uniqueCharacters = new HashSet<>();
        HashSet<Character> charactersSeenSoFar = new HashSet<>();

        for (int i = 0; i < text.length(); i++) {
            char currentChar = text.charAt(i);
            if (!charactersSeenSoFar.contains(currentChar)) {
                charactersSeenSoFar.add(currentChar);
            } else {
                // İki kelime bulunduğunda işlemi sonlandırma
                break;
            }
        }

        uniqueCharacters.addAll(charactersSeenSoFar);
        return uniqueCharacters;
    }
}
