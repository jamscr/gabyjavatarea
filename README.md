# gabyjavatarea

import java.util.*;
import java.text.*;
import java.io.*;
public class JavaApplication2 {


    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {

   
        SimpleDateFormat sdf = new SimpleDateFormat("dd-M-yyyy");
       
        BufferedReader reader= new BufferedReader(
                new InputStreamReader(System.in));
        
        try{
            System.out.print("Digite la fecha(dd-MM-yyyy): ");
            String fecha = reader.readLine();
            
            Date date = sdf.parse(fecha);
 
            Calendar calendar = Calendar.getInstance();
            calendar.setTime(date);

            
            System.out.print("Fecha digitada: ");
            System.out.println(sdf.format(calendar.getTime()));
            
            calendar.add(Calendar.DATE,-8);
            
            System.out.print("Fecha digitada menos 8 días: ");
            System.out.println(sdf.format(calendar.getTime()));            
        }
        catch (Exception e){
            System.out.print("Error de formato");
        }

    }
    
}
