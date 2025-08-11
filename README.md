# Comprehensive-Analysis-of-BERT-Ransomware
BERT ransomware adalah kelompok ancaman siber yang beroperasi dengan model pemerasan ganda (*double extortion*), memadukan enkripsi data korban dan ancaman publikasi informasi sensitif di situs kebocoran data di dark web. Serangan ini bersifat lintas platform, menargetkan sistem Windows dan Linux dengan vektor infeksi utama melalui phishing, eksploitasi kerentanan, dan *malicious updates*. Infrastruktur terorganisir dan teknik multi-stage execution menjadikan BERT salah satu ransomware dengan tingkat kompleksitas dan dampak yang tinggi.

Menurut tulisan yang dimuat pada laman resmi blog.hunterstrategy.net, Attack vector yang digunakan oleh group ransomware ini ada beberapa, dimulai dari Phishing berperan sebagai metode infeksi utama, memanfaatkan teknik rekayasa sosial untuk memperoleh akses awal ke jaringan. Malicious Downloads melibatkan distribusi payload melalui situs web yang telah dikompromikan atau file unduhan berbahaya. Exploiting Vulnerabilities menargetkan kerentanan perangkat lunak yang belum diperbarui (unpatched), khususnya pada layanan yang berjalan di server Linux, untuk mendapatkan kendali sistem. Sementara itu, Malicious Software Updates menggunakan pembaruan perangkat lunak atau keamanan palsu sebagai sarana penyebaran ransomware. Pendekatan multi-vektor ini memungkinkan BERT meningkatkan peluang keberhasilan serangan sekaligus memperluas cakupan target, baik pada lingkungan Windows maupun Linux.

<img width="760" height="572" alt="image" src="https://github.com/user-attachments/assets/3b5052a9-bab5-4774-ad55-1c1ee566cad6" />

Secara umum, infection chain serangan ransomware BERT mengikuti rangkaian tahapan yang terstruktur untuk memastikan infiltrasi, eksekusi, dan dampak maksimal pada sistem target. Tahap pertama dimulai dengan pengiriman phishing email yang menjadi vektor infeksi utama. Email ini dirancang menggunakan teknik social engineering untuk memicu interaksi dari penerima, seperti membujuk korban untuk membuka attachment atau mengklik tautan tertentu. Attachment yang disertakan dapat berupa dokumen berformat Office dengan malicious macro tersemat atau link yang mengarahkan korban ke situs web yang telah dikompromikan. Kedua metode ini memiliki tujuan yang sama, yaitu men-download file berbahaya ke perangkat korban.

 

Setelah file tersebut diunduh dan dijalankan, payload awal biasanya berupa skrip berformat .ps1 (PowerShell script). Skrip ini berisi instruksi berbahaya yang berfungsi untuk melakukan eskalasi hak akses (privilege escalation), memodifikasi konfigurasi sistem, serta menonaktifkan atau mematikan layanan security tools seperti antivirus, EDR (Endpoint Detection and Response), atau firewall. Hal ini dilakukan guna meminimalkan kemungkinan deteksi dan mengamankan jalur eksekusi tahap berikutnya.

<img width="658" height="627" alt="image" src="https://github.com/user-attachments/assets/114f3a22-0b46-48f3-9053-dd7bb0acea4d" />

Tahap selanjutnya adalah proses staging dan pengunduhan komponen inti ransomware dari command and control server (C2). Komponen ini bertanggung jawab untuk memulai proses enkripsi pada file korban, menggunakan algoritma enkripsi yang kuat dan biasanya memodifikasi ekstensi file yang telah terenkripsi. Selain itu, ransomware BERT sering kali meninggalkan catatan tebusan (ransom note) yang berisi instruksi pembayaran dan ancaman terhadap korban, termasuk kemungkinan kebocoran data jika tebusan tidak dibayar.
Pendekatan yang digunakan BERT bersifat multi-stage dan multi-vector, memadukan teknik manipulasi manusia (human-driven attack) dengan eksekusi otomatis berbasis skrip untuk memastikan tingkat keberhasilan yang tinggi. Strategi ini membuat serangan tidak hanya efektif pada lingkungan Windows, tetapi juga dapat diperluas ke sistem berbasis Linux, sehingga memperbesar cakupan target dan dampaknya.



