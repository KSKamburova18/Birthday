# Birthday

import java.util.Scanner;
import java.util.List;
import java.util.ArrayList;
public class Main {


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<String[]> wordArray = new ArrayList<>();
        while(true) {
            String fullString = sc.nextLine();
            if (fullString.equalsIgnoreCase("end"))
                break;
            wordArray.add(sc.nextLine().split(" "));
        }
            String inputYear = sc.next()
            for (String[] word : wordArray) {
                String year = null;
                switch (word[0]) {
                    case "Citizen":
                        year = word[4].split("/")[2];
                        break;
                    case "Pet":
                        year = word[2].split("/")[2];
                        break;
                }

                if (year != null){
                    if(inputYear.equals(year)) {
                        switch (word[0]) {
                            case "Citizen":
                               System.out.println(word[4]);
                                break;
                            case "Pet":
                                System.out.println(word[2]);
                                break;
                        }
                    }
                }
            }
    }
}

public interface Birthable {
    public String getBirthable();
}


public interface Identifiable {
    public String getIf();
}


    private String name;
    private int age;
    private String id;
    private String birthDate;

    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    public String getId() {
        return id;
    }

    public Citizen(String name, int age, String id, String birthDate) {
        this.name = name;
        this.age = age;
        this.id = id;
        this.birthDate = birthDate;
    }
}

public class Robot implements Identifiable{

    private String id;
    private String model;

    public Robot(String id, String model) {
        this.id = id;
        this.model = model;
    }

    public String getId() {
        return id;
    }

    public String getModel() {
        return model;
    }
}

public class Pet implements Birthable{
    private String name;
    private String birthDate;

    public Pet(String name, String birthDate) {
        this.name = name;
        this.birthDate = birthDate;
    }

    public String getName() {
        return name;
    }

    public String getBirthDate() {
        return birthDate;
    }
}
