# Quiz Dasar Widget

Uji pemahamanmu tentang materi yang telah dipelajari di bab Dasar Widget ini! Pilih jawaban yang paling tepat, lalu tekan tombol periksa di bawah setiap pertanyaan.

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>1. Widget manakah yang tepat digunakan untuk menyusun urutan elemen secara berderet menurun dari atas ke bawah?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="a"> a) Row</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="b"> b) Column</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="c"> c) Expanded</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="d"> d) Container</label></div>
  <button type="button" onclick="cekJawaban('q1')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q1" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>2. Jika kita sudah menyimpan gambar resmi di dalam folder proyek komputermu sendiri (tanpa butuh jaringan internet), perintah apa yang benar untuk memanggilnya?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="a"> a) Image.asset()</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="b"> b) Image.network()</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="c"> c) Icon()</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="d"> d) GambarLokal()</label></div>
  <button type="button" onclick="cekJawaban('q2')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q2" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>3. Perintah navigasi apa yang digunakan saat sebuah layar profil siswa ingin ditutup untuk mundur kembali menatap layar beranda sebelumnya?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="a"> a) Navigator.push</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="b"> b) Navigator.pop</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="c"> c) setState</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="d"> d) Expanded</label></div>
  <button type="button" onclick="cekJawaban('q3')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q3" style="margin-top: 15px;"></div>
</div>

<script>
const quizData = {
  q1: {
    correct: 'b',
    explanations: {
      a: '<strong>Row</strong> digunakan untuk menyusun deret elemen menyamping secara horizontal (dari kiri ke kanan).',
      b: '<strong>Tepat sekali!</strong> <strong>Column</strong> dirancang khusus sebagai struktur penyusun tumpukan elemen vertikal (atas ke bawah).',
      c: '<strong>Expanded</strong> digunakan untuk mengatur sisa ruang kosong pada layout, bukan untuk menyusun elemen.',
      d: '<strong>Container</strong> adalah kotak pembungkus yang hanya bisa memuat satu anak *widget* saja.'
    }
  },
  q2: {
    correct: 'a',
    explanations: {
      a: '<strong>Tepat sekali!</strong> <strong>Image.asset</strong> digunakan untuk memanggil foto secara lokal yang sudah didaftarkan di dalam *file* pubspec.yaml.',
      b: '<strong>Image.network</strong> membutuhkan koneksi internet untuk menampilkan gambar dari tautan web.',
      c: '<strong>Icon</strong> hanya diperuntukkan bagi logo grafis kecil bawaan Flutter.',
      d: '<strong>GambarLokal()</strong> bukanlah fungsi *widget* yang ada pada Flutter.'
    }
  },
  q3: {
    correct: 'b',
    explanations: {
      a: '<strong>Navigator.push</strong> digunakan untuk maju berpindah dan menumpuk halaman baru di atas halaman saat ini.',
      b: '<strong>Tepat sekali!</strong> <strong>Navigator.pop</strong> berfungsi menutup atau membuang halaman aktif agar kita kembali ke layar sebelumnya.',
      c: '<strong>setState</strong> bertugas menyegarkan tampilan data di halaman yang sama, bukan untuk berpindah halaman.',
      d: '<strong>Expanded</strong> tidak berkaitan dengan fitur navigasi layar aplikasi.'
    }
  }
};

function cekJawaban(questionId) {
  const options = document.getElementsByName(questionId);
  let selectedValue = '';
  
  for (let i = 0; i < options.length; i++) {
    if (options[i].checked) {
      selectedValue = options[i].value;
      break;
    }
  }
  
  const feedbackDiv = document.getElementById('feedback-' + questionId);
  
  if (selectedValue === '') {
    feedbackDiv.innerHTML = '<span style="color: rgba(230, 126, 34, 1); font-weight: bold;">Tentukan salah satu opsi pilihan jawaban terlebih dahulu!</span>';
    return;
  }
  
  const qData = quizData[questionId];
  const isCorrect = selectedValue === qData.correct;
  const penjelasanSpesifik = qData.explanations[selectedValue];
  
  let resultText = '';
  if (isCorrect) {
    resultText = '<span style="color: rgba(39, 174, 96, 1); font-weight: bold; font-size: 1.1em;">Benar.</span><br>';
  } else {
    resultText = '<span style="color: rgba(192, 57, 43, 1); font-weight: bold; font-size: 1.1em;">Salah.</span><br>';
  }
  
  const explanationBox = '<div style="margin-top: 15px; padding: 15px; background-color: rgba(128, 128, 128, 0.1); border-left: 5px solid rgba(41, 128, 185, 0.8); font-size: 0.95em; line-height: 1.5; color: inherit;">' + penjelasanSpesifik + '</div>';
  
  feedbackDiv.innerHTML = resultText + explanationBox;
}
</script>
