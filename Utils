import.java.security.PrivateKey;
import.java.security.spec.EncodedKeySpec;
import.java.security.spec.X509EncodedKeySpec;
import.java.util.Base64;

public class Utils {
  
  public static final String destination_IP = "127.0.0.1";
  
  public static void main(String[] args) { }
  
  public static PrivateKey getPrivKey() throws Exception {
    byte[] priv_key = "insert_EC_private_key".getBytes();
    String encoded_key = new String(priv_key, "UTF-8");
    byte[] key_bytes = Base64.getDecorder().decode(encoded_key);
    PKCS8EncodedKeySpec spec = new PKCS8EncodedKeySpec(key_bytes);
    KeyFactory kf = new KeyFactory.getInstance("EC");
    PrivateKey = priv_key = kf.generatePrivate(spec);
    return PrivateKey;
  }
}
