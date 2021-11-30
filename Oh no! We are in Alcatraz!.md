# Oh no! We are in Alcatraz"

_Oof, you have just been arrested for treason and you are now stranded in Alcatraz. Can you make it out alive? Read the attached code and try find the flag!_

This problem comes with a .java file that contains some java code. The only relevant part to solving this flag is this:

`       byte[] myBytes = {
            117, 95, 106, 48, 105, 110, 105 ,    
            0x6e, 0x67, 0x5f, 0x61, 0x6e, 0x30, 
            0156, 0171, 0155, 060, 0165,    
            's' , '_', 's','0', '0', 'n', '?',
        };`


Converting these bytes to hex by using

`for(int i = 0; i < myBytes.length; i++){
            System.out.print(Integer.toHexString((myBytes[i] & 0xFF)));
        }`

gives us this hex string:

755f6a30696e696e675f616e306e796d3075735f7330306e3f

Converting this hex string to ascii gives us the flag

Flag is flag{u_j0ining_an0nym0us_s00n?}
