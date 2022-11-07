# codepatrick


import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;


public class Ausgabedatei {

	
	public static void main(String args []) {
		
		File datei = new File("C:/Users/patri/Documents/files/klausur.csv");
		
		System.out.println(datei.isFile()); 
		Scanner scan = null;
		
		try {
		scan = new Scanner(datei).useDelimiter(";");
		
		}catch (FileNotFoundException exception) {
			
			System.out.println("Datei wurde nicht gefunden");
			
		}
		
		
		
		
		while(scan.hasNextLine()) {
		System.out.println(scan.nextLine());
        int Matrikelnummer = scan.nextInt();
        String vorname = scan.next();
		String nachname = scan.next();
		int note = scan.nextInt();
		Student patrick = new Student(Matrikelnummer,vorname,nachname,note);
		}
		
		
		
	}
	
	
	
}



