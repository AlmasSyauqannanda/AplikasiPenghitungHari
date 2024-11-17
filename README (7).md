
## Aplikasi Sederhana untuk Menghitung Jumlah Huruf, Kata, Kalimat, dan Paragraf
Aplikasi ini dirancang untuk membantu pengguna menghitung elemen-elemen dalam teks seperti jumlah huruf, kata, kalimat, dan paragraf dengan cepat dan akurat. Dengan antarmuka yang sederhana, pengguna dapat memasukkan teks secara langsung untuk mendapatkan hasil perhitungan. Cocok untuk penulis, pelajar, atau siapa saja yang memerlukan analisis cepat pada dokumen teks.

# Deskripsi
Aplikasi ini memberikan kemudahan bagi pengguna untuk menganalisis teks secara sederhana. Pengguna dapat menghitung jumlah kata, karakter, kalimat, paragraf, dan bahkan mencari jumlah kemunculan kata tertentu. Dengan fitur pencarian kata yang disediakan, aplikasi ini menjadi solusi ideal untuk kebutuhan analisis teks dasar.






## Features
Input Teks
Pengguna dapat mengetik atau menempelkan teks langsung ke dalam area input yang disediakan.

Penghitungan Jumlah Elemen Teks
Aplikasi menghitung jumlah:

Kata
Karakter
Kalimat
Paragraf
Pencarian Kata Tertentu
Pengguna dapat memasukkan kata yang ingin dicari dalam teks dan mendapatkan jumlah kemunculannya secara instan.

Tombol Hitung
Tersedia tombol untuk memproses semua perhitungan sekaligus dengan satu klik.

Tombol Simpan
Memungkinkan pengguna untuk menyimpan teks yang telah dimasukkan untuk keperluan lebih lanjut.

## Teknologi yang Digunakan
Masukkan teks ke dalam area input.
Klik tombol Hitung untuk mendapatkan hasil perhitungan elemen teks.
Jika ingin mencari jumlah kemunculan kata tertentu, masukkan kata pada kolom pencarian dan klik tombol Cari.
Hasil perhitungan akan muncul di bagian yang sesuai.
Klik tombol Simpan untuk menyimpan teks ke file atau database.
Teknologi yang Digunakan
GUI (Graphical User Interface):
Dibangun menggunakan pustaka GUI seperti Tkinter, PyQt, atau teknologi Java Swing untuk memberikan pengalaman pengguna yang interaktif dan sederhana.

Pemrosesan Teks:
Menggunakan algoritma berbasis string untuk menganalisis jumlah elemen teks dengan presisi.## Aplikasi Sederhana untuk Menghitung Jumlah Huruf, Kata, Kalimat, dan Paragraf
public class HitungKataKarakter extends javax.swing.JFrame {

    /**
     * Creates new form HitungKataKarakter
     */
    public HitungKataKarakter() {
        initComponents();
        
    }
      private void hitungJumlah() {
        String text = textAreaInput.getText();
        
        // Menghitung jumlah karakter
        int jumlahKarakter = text.length();
        
        // Menghitung jumlah kata menggunakan ekspresi reguler
        String[] words = text.trim().split("\\s+");
        int jumlahKata = (words.length == 1 && words[0].equals("")) ? 0 : words.length;
        
         // Menghitung jumlah kalimat (menggunakan tanda titik, tanda seru, atau tanda tanya sebagai akhir kalimat)
        String[] kalimat = text.trim().split("[.!?]");
        int jumlahKalimat = (kalimat.length == 1 && kalimat[0].equals("")) ? 0 : kalimat.length;
        
        // Menghitung jumlah paragraf (menggunakan dua baris baru berturut-turut sebagai pemisah paragraf)
        String[] paragraf = text.trim().split("\\n\\s*\\n");
        int jumlahParagraf = (paragraf.length == 1 && paragraf[0].equals("")) ? 0 : paragraf.length;
        
        
        // Menampilkan hasil pada JLabel
        lblJumlahKata.setText("Jumlah Kata: " + jumlahKata);
        lblJumlahKarakter.setText("Jumlah Karakter: " + jumlahKarakter);
        Kalimat2.setText("Jumlah Kalimat: " + jumlahKalimat);
        paragraf2.setText("Jumlah Paragraf: " + jumlahParagraf);
    }
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jPanel1 = new javax.swing.JPanel();
        lblJumlahKata = new javax.swing.JLabel();
        lblJumlahKarakter = new javax.swing.JLabel();
        btnHitung = new javax.swing.JButton();
        jScrollPane2 = new javax.swing.JScrollPane();
        textAreaInput = new javax.swing.JTextArea();
        Kalimat2 = new javax.swing.JLabel();
        paragraf2 = new javax.swing.JLabel();
        textFieldCari = new javax.swing.JTextField();
        jLabel1 = new javax.swing.JLabel();
        btnCari = new javax.swing.JButton();
        lblPencarian = new javax.swing.JLabel();
        btnSimpan = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        lblJumlahKata.setText("Jumlah kata");

        lblJumlahKarakter.setText("Jumlah karakter");

        btnHitung.setText("Hitung");
        btnHitung.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnHitungActionPerformed(evt);
            }
        });

        textAreaInput.setColumns(20);
        textAreaInput.setRows(5);
        jScrollPane2.setViewportView(textAreaInput);

        Kalimat2.setText("jumlah kalimat");

        paragraf2.setText("jumlah paragraf");

        jLabel1.setText("Kata yang di cari");

        btnCari.setText("Cari");
        btnCari.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnCariActionPerformed(evt);
            }
        });

        lblPencarian.setText("Hasil");

        btnSimpan.setText("Simpan");
        btnSimpan.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnSimpanActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addGap(25, 25, 25)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(jScrollPane2, javax.swing.GroupLayout.PREFERRED_SIZE, 398, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(34, 34, 34))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, jPanel1Layout.createSequentialGroup()
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(btnSimpan)
                        .addGap(201, 201, 201)))
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(lblJumlahKata)
                    .addComponent(lblJumlahKarakter)
                    .addComponent(btnHitung)
                    .addComponent(Kalimat2)
                    .addComponent(paragraf2))
                .addGap(71, 71, 71)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jLabel1)
                    .addComponent(textFieldCari, javax.swing.GroupLayout.PREFERRED_SIZE, 92, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(btnCari)
                    .addComponent(lblPencarian))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );
        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addGap(21, 21, 21)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(28, 28, 28)
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(lblJumlahKata)
                            .addComponent(jLabel1))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(lblJumlahKarakter)
                            .addComponent(textFieldCari, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(Kalimat2)
                            .addComponent(btnCari))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(paragraf2)
                            .addComponent(lblPencarian))
                        .addGap(67, 67, 67)
                        .addComponent(btnHitung))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(jScrollPane2, javax.swing.GroupLayout.PREFERRED_SIZE, 163, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(18, 18, 18)
                        .addComponent(btnSimpan)))
                .addContainerGap(51, Short.MAX_VALUE))
        );

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap(54, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(46, 46, 46)
                .addComponent(jPanel1, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addContainerGap())
        );

        pack();
    }// </editor-fold>                        

    private void btnHitungActionPerformed(java.awt.event.ActionEvent evt) {                                          
         hitungJumlah();
    }                                         

    private void btnCariActionPerformed(java.awt.event.ActionEvent evt) {                                        
        String text = textAreaInput.getText();
    String kataCari = textFieldCari.getText().trim();

    if (!kataCari.isEmpty()) {
        // Menghitung jumlah kemunculan kata yang dicari
        String[] words = text.split("\\s+");
        int count = 0;
        for (String word : words) {
            if (word.equalsIgnoreCase(kataCari)) {
                count++;
            }
        }

        // Menampilkan hasil pencarian
        lblPencarian.setText("Kata '" + kataCari + "' ditemukan sebanyak " + count + " kali.");
    } else {
        lblPencarian.setText("Masukkan kata yang ingin dicari.");
    }
    
    btnSimpan = new javax.swing.JButton();
    btnSimpan.setText("Simpan ke File");
    btnSimpan.addActionListener(new java.awt.event.ActionListener() {
    public void actionPerformed(java.awt.event.ActionEvent evt) {
        btnSimpanActionPerformed(evt);
    }
});
    }                                       

    private void btnSimpanActionPerformed(java.awt.event.ActionEvent evt) {                                          
            // Mendapatkan teks dan hasil perhitungan
    String text = textAreaInput.getText();
    String jumlahKata = lblJumlahKata.getText();
    String jumlahKarakter = lblJumlahKarakter.getText();
    String jumlahKalimat = Kalimat2.getText();
    String jumlahParagraf = paragraf2.getText();
    String hasilPencarian = lblPencarian.getText();

    // Menggabungkan semua hasil menjadi satu string untuk disimpan
    String hasil = "Teks:\n" + text + "\n\n"
                 + jumlahKata + "\n"
                 + jumlahKarakter + "\n"
                 + jumlahKalimat + "\n"
                 + jumlahParagraf + "\n"
                 + hasilPencarian + "\n";

    // Memilih lokasi dan nama file untuk menyimpan
    javax.swing.JFileChooser fileChooser = new javax.swing.JFileChooser();
    int option = fileChooser.showSaveDialog(this);
    if (option == javax.swing.JFileChooser.APPROVE_OPTION) {
        try {
            // Menyimpan hasil ke file
            java.io.File file = fileChooser.getSelectedFile();
            java.io.FileWriter writer = new java.io.FileWriter(file);
            writer.write(hasil);
            writer.close();
            javax.swing.JOptionPane.showMessageDialog(this, "Data berhasil disimpan!");
        } catch (java.io.IOException e) {
            javax.swing.JOptionPane.showMessageDialog(this, "Gagal menyimpan data: " + e.getMessage());
        }
    }
    }                                         

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(HitungKataKarakter.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(HitungKataKarakter.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(HitungKataKarakter.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(HitungKataKarakter.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new HitungKataKarakter().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JLabel Kalimat2;
    private javax.swing.JButton btnCari;
    private javax.swing.JButton btnHitung;
    private javax.swing.JButton btnSimpan;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JScrollPane jScrollPane2;
    private javax.swing.JLabel lblJumlahKarakter;
    private javax.swing.JLabel lblJumlahKata;
    private javax.swing.JLabel lblPencarian;
    private javax.swing.JLabel paragraf2;
    private javax.swing.JTextArea textAreaInput;
    private javax.swing.JTextField textFieldCari;
    // End of variables declaration                   
}

## Authors

- [@AlmasSyauqannanda](https://www.github.com/AlmasSyauqannanda)

