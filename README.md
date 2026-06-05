Masalah Sebelum Refactoring
Poor Naming
Nama fungsi dan variabel tidak deskriptif sehingga sulit dipahami.
Contoh: proc(), o, t, d.
Long Method
Fungsi utama menangani terlalu banyak proses sekaligus, seperti perhitungan subtotal, diskon, pajak, dan biaya pengiriman.
Melanggar prinsip Single Responsibility.
Magic Numbers
Nilai diskon dan biaya pengiriman ditulis langsung dalam kode (10, 5, 200).
Sulit diubah dan dipelihara.
Duplicate Code
Logika perhitungan diskon ditulis berulang untuk setiap jenis diskon.
Difficult to Test
Semua logika berada dalam satu fungsi sehingga sulit dilakukan pengujian unit (unit testing).
Perbaikan Setelah Refactoring
Refactoring Poor Naming
Mengubah nama fungsi dan variabel menjadi lebih deskriptif.
Contoh:
proc() → processOrder()
o → orderItems
d → discountType
Refactoring Long Method
Memecah fungsi besar menjadi beberapa fungsi kecil:
calculateSubtotal()
applyDiscount()
calculateFinalTotal()
Refactoring Magic Numbers
Mengganti nilai hardcoded menjadi konstanta:
STUDENT_DISCOUNT
MEMBER_DISCOUNT
SHIPPING_COST
Refactoring Duplicate Code
Membuat struktur mapping diskon dan fungsi khusus untuk perhitungan diskon sehingga logika tidak berulang.
Improved Testability
Setiap fungsi memiliki satu tanggung jawab dan dapat diuji secara independe
