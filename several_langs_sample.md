

#Java 
```Java
import java.io.BufferedWriter;
import java.io.File;
import java.io.FileOutputStream;
import java.io.FileWriter;
import java.io.IOException;
import java.io.OutputStream;
import java.nio.file.Files;
import java.nio.file.Paths;

public class WriteFile {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        
        // считать сообщение
        String userMessage = in.nextString();
        
        try {
            // открыть файл
            PrintWriter out = new PrintWriter("/tmp/ourfile.txt");
            
            // записать туда строку
            out.println(userMessage);
            
            // сохранить файл
            out.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
        
        // вывести оповещение о сохранении сообщения
        System.out.println("Сообщение сохранено");
    }
}


#Python
```python
print("Hello World")
# считать сообщение
userMessage = input()
# открыть файл
file = open("/tmp/ourfile.txt", "w")
# записать туда строку
file.Write(userMessage)
# сохранить файл
file.close()
# вывести оповещение о сохранении сообщения
print("Сообщение сохранено")
