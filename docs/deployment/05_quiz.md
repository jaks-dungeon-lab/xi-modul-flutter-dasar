# Quiz Deployment

Uji pemahamanmu tentang materi wawasan akhir pengembang aplikasi di bab ini! Pilih jawaban yang paling tepat, lalu tekan tombol periksa di bawah setiap pertanyaan.

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>1. Jika kita selesai membuat aplikasi Flutter di komputer Windows lab sekolah, format file apa yang bisa langsung kita hasilkan untuk dibagikan ke HP teman kita?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="a"> a) EXE</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="b"> b) IPA</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="c"> c) APK</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q1" value="d"> d) HTML</label></div>
  <button type="button" onclick="cekJawaban('q1')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q1" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>2. Mengapa kita tidak disarankan atau tidak bisa merakit file iOS (IPA) menggunakan laptop bersistem operasi Windows?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="a"> a) Karena Windows terlalu lambat untuk memproses kode Apple</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="b"> b) Karena proses pembuatan IPA wajib membutuhkan sistem macOS dan aplikasi Xcode</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="c"> c) Karena Windows tidak memiliki kabel data yang cocok untuk iPhone</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q2" value="d"> d) Karena Flutter belum mendukung pembuatan aplikasi Apple</label></div>
  <button type="button" onclick="cekJawaban('q2')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q2" style="margin-top: 15px;"></div>
</div>

<div class="question-block" style="margin-bottom: 25px; padding: 20px; border: 1px solid rgba(128, 128, 128, 0.3); border-radius: 8px;">
  <p style="margin-bottom: 15px; font-size: 1.05em;"><strong>3. Perintah apa yang harus diketikkan pada terminal jika kita ingin mengubah aplikasi Flutter menjadi halaman situs internet yang bisa dihosting?</strong></p>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="a"> a) flutter run web</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="b"> b) flutter create web</label></div>
  <div style="margin-bottom: 8px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="c"> c) flutter make html</label></div>
  <div style="margin-bottom: 15px;"><label style="cursor: pointer;"><input type="radio" name="q3" value="d"> d) flutter build web</label></div>
  <button type="button" onclick="cekJawaban('q3')" style="padding: 8px 16px; background-color: rgba(41, 128, 185, 0.8); color: white; border: none; border-radius: 4px; cursor: pointer;">Cek Jawaban</button>
  <div id="feedback-q3" style="margin-top: 15px;"></div>
</div>

<script>
const quizData = {
  q1: {
    correct: 'c',
    explanations: {
      a: '<strong>EXE</strong> adalah format program komputer desktop khusus Windows, bukan format yang dipakai untuk telepon genggam Android.',
      b: '<strong>IPA</strong> adalah format eksklusif untuk dipasang ke dalam perangkat Apple iPhone (iOS), yang tidak dapat diciptakan dari lingkungan komputer murni Windows.',
      c: '<strong>Tepat sekali!</strong> <strong>APK</strong> adalah format standar Android yang dapat dirakit lewat perintah `flutter build apk` di dalam sistem operasi komputer apa pun secara universal.',
      d: '<strong>HTML</strong> adalah format dokumen bacaan web, ia tidak dirancang khusus sebagai bungkus bentuk peranti lunak ponsel untuk dipasang langsung ke dalam menu HP.'
    }
  },
  q2: {
    correct: 'b',
    explanations: {
      a: 'Kecepatan laptop Windows sama sekali bukanlah faktor pembatas; yang menjadi penengah larangan ini adalah pembatas izin keamanan kaku dari perusahaan Apple sendiri.',
      b: '<strong>Tepat sekali!</strong> Syarat mutlak meracik bangunan mesin iPhone adalah keberadaan aplikasi resmi <strong>Xcode</strong>, di mana alat tersebut hanya berlisensi ditanam di sistem operasi komputer Apple (macOS).',
      c: 'Ini keliru. Laptop Windows bisa menggunakan kabel USB iPhone biasa untuk memindahkan foto, namun tetap tidak diizinkan memiliki mesin cetak aplikasinya secara legal.',
      d: 'Flutter sudah sejak awal menasbihkan dirinya sebagai pembangun tangguh aplikasi iOS; halangannya terletak di alat cetak wajibnya, bukan pada bahasa pemrograman Flutter-nya.'
    }
  },
  q3: {
    correct: 'd',
    explanations: {
      a: '<strong>flutter run web</strong> sekadar membuka wujud tampilannya untuk uji coba sesaat di layar laptopmu; tapi perintah ini tidak akan mencetak file jadinya ke dalam lemari untuk diunggah permanen.',
      b: '<strong>flutter create web</strong> bukanlah perintah mencetak produk, namun digunakan di awal untuk melahirkan merakit fondasi folder proyek saat baru pertama kali dibuat.',
      c: '<strong>flutter make html</strong> adalah perintah rekayasa imajiner yang tidak ada di dalam daftar kode resmi perintah Flutter.',
      d: '<strong>Tepat sekali!</strong> Perintah <strong>flutter build web</strong> adalah satu-satunya mantra sejati penggerak oven cetak untuk memasak kodemu menjadi gabungan format murni HTML dan JS di dalam folder `/build/web`.'
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
