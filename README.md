# StudiCase

Nama :alfarid p.yusuf
NIM  :19.11.2841
KELAS:19-IF-04

Aplikasi Promos keranjang/kasir sederhana yang juga merupakan modifikasi aplikasi di repo sebelumnya dan sekarang memperbaiki dengan menambahkan beberapa fitur baru

# Algoritma
 User pertama kali akan ditampilkan halaman mainwindow yang berisikan keranjang, serta subtotal dan total harga. Serta opsi untuk memilih voucher yang tersedia.
 kemudian user akan memilih item pada halaman penawaran yang kemudian item tersebut akan masuk ke dalam keranjang (user dapat menghapus item jika ada kesalahan)
 Lanjut dengan pemilihan voucher sebagai akhir dari alur aplikasi serta penggunaannya untuk pemotongan harga pada total.


        public MainWindow()
        {
            InitializeComponent();

            payment = new Payment(this);

            KeranjangBelanja keranjangBelanja = new KeranjangBelanja(payment, this);

            controller = new MainWindowController(keranjangBelanja);

            listBoxPesanan.ItemsSource = controller.getSelectedItems();
            listBoxPakaiVoucher.ItemsSource = controller.getSelectedVouchers();

            initializeView();

# Kegunaan
- User dapat memilih, serta menghapus item pada keranjang
- User dapat memilih voucher untuk pemotongan harga




