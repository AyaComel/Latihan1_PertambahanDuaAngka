# Latihan1_PertambahanDuaAngka
 Latihan 1-Cahya Hayyuni-2210010118
 
## 1. Deskripsi Program:
  • Pengguna memasukkan dua angka
• Saat tombol Tambah diklik akan menampilkan hasil pertambahan
• Saat tombol Hapus diklik akan menghapus nilai di TextField dan
mengarahkan fokus ke TextField angka pertama

## 2. Komponen GUI: 
JFrame, JPanel, JLabel, JTextField, JButton

## 3. Logika Program:
Penambahan dua angka, validasi input numerik

## 4. Events:
-ActionListener untuk tombol Tambah, Hapus, dan Keluar
A.Tambah
~~~
private void btnTambahActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:
        try {
        int angka1 = Integer.parseInt(txtAngka1.getText());
        int angka2 = Integer.parseInt(txtAngka2.getText());
        int hasil = angka1 + angka2;
        txtHasil.setText(String.valueOf(hasil));
~~~
B.Hapus
~~~
private void btnHapusActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        txtAngka1.setText("");
        txtAngka2.setText("");
        txtHasil.setText("");
        txtAngka1.requestFocus();
    }  
~~~
C.Keluar
~~~
private void btnKeluarActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:
        System.exit(0);
    }                                         
~~~
5. Variasi:
A.KeyAdapter pada JTextField untuk membatasi input hanya angka
~~
    // TODO add your handling code here:
        char c = evt.getKeyChar();
        if (!Character.isDigit(c) && c != KeyEvent.VK_BACK_SPACE && c != KeyEvent.VK_DELETE) {
            evt.consume();
            JOptionPane.showMessageDialog(this, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
        }
    } 
~~~
B.Gunakan JOptionPane untuk menampilkan error input
~~~
} catch (NumberFormatException e) {
        JOptionPane.showMessageDialog(this, "Input harus berupa angka!", "Error", JOptionPane.ERROR_MESSAGE);
    }
~~~
C.Implementasikan FocusListener untuk membersihkan JTextField
saat mendapatkan fokus.
~~~
    private void txtAngka1FocusGained(java.awt.event.FocusEvent evt) {                                      
        // TODO add your handling code here:
        txtAngka1.setText("");
    }
 ~~~

## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Kesesuaian UI    |    15    |
|  4  | Constructor      |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

Nama:
NPM:
