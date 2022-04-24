import java.io.IOException;
import java.io.PrintWriter;
import java.net.Socket;
import java.security.PrivateKey;
import java.security.SecureRandom;
import.java.security.Signature;

// Generate a 10 digit cryptographic nonce
SecureRandom random = new SecureRandom();
StringBuilder sb = new StringBuilder();
for (int i=0; i<10; i++) {
    stringBuilder.append(random.nextInt(10));
}
server_nonce = sb.toString();

// Load private key
PrivateKey priv_key = Utils.getPrivateKey();
Signature signature = Signature.getinstance("SHA256withECDSA");

// Create message
server_msg = "Hello" + server_nonce;

// Sign the message
server_msg = server_msg.getBytes("UTF-8");
signature.initSign(priv_key);
signature.update(server_msg);
server_signature = signature.sign();    // This is the digital siganture

// Sending plaintext message and append digital signature
server_msg = server_msg + Base64.getEncoder().encodeToString(server_signature);

try {
    socket = new Socket(Utils.destination_IP, 17000);
    pw = new PrintWriter(socket.getOutputStream());
    pw.write(server_msg);
    pw.flush();
    pw.close();
    s.close();
} catch (IOException e) {
    e.printStackTrace();
}
