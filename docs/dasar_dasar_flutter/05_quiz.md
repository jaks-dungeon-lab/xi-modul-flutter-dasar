# Quiz Dasar-Dasar Flutter

Uji pemahamanmu tentang materi yang telah dipelajari! Pilih jawaban yang paling tepat, lalu klik tombol cek di bawah setiap pertanyaan. Kamu bisa mengubah jawaban jika mau.

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>1. Di folder manakah kamu biasanya menuliskan kode bahasa pemrograman Dart pada proyek Flutter?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="a"> a) ios/</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="b"> b) lib/</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="c"> c) web/</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="d"> d) test/</label></div>
  <button type="button" onclick="cekJawaban('q1')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q1" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>2. Widget apakah yang digunakan untuk membuat tampilan dinamis yang bisa berubah karena interaksi (contoh: angka bertambah)?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="a"> a) StatelessWidget</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="b"> b) StatefulWidget</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="c"> c) Scaffold</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="d"> d) MaterialApp</label></div>
  <button type="button" onclick="cekJawaban('q2')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q2" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>3. Perintah terminal apa yang wajib dijalankan untuk mengunduh package setelah kamu memperbarui file pubspec.yaml?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="a"> a) flutter run</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="b"> b) flutter pub add</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="c"> c) flutter pub get</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="d"> d) flutter upgrade</label></div>
  <button type="button" onclick="cekJawaban('q3')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q3" style="margin-top: 15px;"></div>
</div>

<script>
const quizData = {
  q1: {
    correct: 'b',
    explanations: {
      a: '<strong>ios/</strong> digunakan untuk konfigurasi spesifik perangkat iOS, bukan tempat menulis kode logika aplikasi.',
      b: '<strong>Tepat sekali!</strong> Folder <strong>lib/</strong> adalah "meja kerja" utama tempat kamu menuliskan semua kode bahasa pemrograman Dart.',
      c: '<strong>web/</strong> berisi konfigurasi untuk menjalankan aplikasi di *browser*, bukan tempat utama untuk kode Dart.',
      d: '<strong>test/</strong> digunakan khusus untuk menulis kode otomatis pengujian aplikasi, bukan logika utama aplikasi.'
    }
  },
  q2: {
    correct: 'b',
    explanations: {
      a: '<strong>StatelessWidget</strong> hanya digunakan untuk tampilan statis yang tidak pernah berubah setelah dirender.',
      b: '<strong>Tepat sekali!</strong> <strong>StatefulWidget</strong> dirancang khusus agar tampilannya bisa dirender ulang ketika terjadi interaksi (menggunakan fungsi setState).',
      c: '<strong>Scaffold</strong> adalah kerangka penyedia AppBar, Body, dll, bukan *widget* pengatur status dinamis.',
      d: '<strong>MaterialApp</strong> adalah pembungkus utama aplikasi dan pengatur tema/rute, bukan untuk interaksi komponen spesifik.'
    }
  },
  q3: {
    correct: 'c',
    explanations: {
      a: '<strong>flutter run</strong> digunakan untuk menjalankan dan menampilkan aplikasi di emulator atau perangkat.',
      b: '<strong>flutter pub add</strong> digunakan untuk mencari dan memasukkan *package* baru secara otomatis ke pubspec.yaml sekaligus mengunduhnya.',
      c: '<strong>Tepat sekali!</strong> Perintah <strong>flutter pub get</strong> wajib dijalankan agar komputer mengunduh *package* yang telah ditambahkan ke pubspec.yaml.',
      d: '<strong>flutter upgrade</strong> digunakan untuk memperbarui versi Flutter SDK, bukan untuk *package* di proyek.'
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
    feedbackDiv.innerHTML = '<span style="color: rgba(230, 126, 34, 1); font-weight: bold;">Pilih jawaban terlebih dahulu.</span>';
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
