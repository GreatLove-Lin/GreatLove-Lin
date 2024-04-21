public class ToolSet {
    
    //字符串转十六进制
    public static String convertStringToHexadecimal(String text) {
        StringBuilder hexString = new StringBuilder();
        for (char c : text.toCharArray()) {
            if(hexString.length()>0){
                hexString.append("-");
            }
            hexString.append(Integer.toHexString(c));
        }
        return hexString.toString();
    }

    //十六进制转字符
    public static String hexadecimalToString(String text){
        String[] split=text.split("-");
        text="";
        for(String str:split){
            //if(str.length()>2){
            text+=new String(Character.toChars(Integer.parseInt(str, 16)));//+new String(Character.toChars(Integer.parseInt(str.substring(2,4), 16)));
            /*}else{
             text+=new String(new BigInteger(str, 16).toByteArray());
             }*/
        }
        return text;
    }
    
    
}
