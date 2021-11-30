# Can you hack for real or for real?

_Try and figure out the password to Fort Knox with the attached file..."_

The attached file is a .java file that has this code:

import java.util.*;

class Knox {
    public static void main(String args[]) {
        Knox fortknox= new Knox();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter Fort Knox password: ");
        String userInput = scanner.next();
        String input = userInput.substring("flag{".length(),userInput.length()-1);
        if (fortknox.checkPassword(input)) {
            System.out.println("Success!");
        } else {
            System.out.println("Failed. The State troopers will be heading here now.");
        }
    }

    // Fort Knox is protected by the United States Department of Defence.
    // Any attempts to crack the password will be punished by the full force of the law.
    // God bless America.
    public boolean checkPassword(String password) {
        return password.length() == 29 &&
               password.charAt(0)  == 'd' &&
               password.charAt(4)  == '_' &&
               password.charAt(2)  == 'e' && 
               password.charAt(23) == 't' &&
               password.charAt(3)  == 's' &&a
               password.charAt(17) == 'd' &&
               password.charAt(1)  == '3' &&
               password.charAt(7)  == '3' &&
               password.charAt(10) == 'c' &&
               password.charAt(5)  == 'a' &&
               password.charAt(9)  == 'i' &&
               password.charAt(11) == 'a' &&
               password.charAt(15) == 'u' &&
               password.charAt(8)  == 'r' &&
               password.charAt(12) == '_' &&                                                                  
               password.charAt(14) == '0' &&                                                                  
               password.charAt(6)  == 'm' &&                                                                  
               password.charAt(24) == 'o' &&
               password.charAt(18) == '_' &&
               password.charAt(13) == 's' &&
               password.charAt(19) == 'c' &&
               password.charAt(21) == '0' &&
               password.charAt(16) == 'n' &&
               password.charAt(27) == 'u' &&
               password.charAt(25) == 'y' &&
               password.charAt(22) == 'l' &&
               password.charAt(28) == '?' &&
               password.charAt(20) == '0' &&
               password.charAt(26) == 'o';
               
    }
}

Piecing together the java code gives us the flag.

Flag is flag{d3es_am3rica_s0und_c00ltoyou?} 
