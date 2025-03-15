Aplikasi Happy Birthday Menggunakan Bahasa Kotlin Menggunakan Android Studio
by : 
Yasmin Putri 
5025221273

1. Membuat Proyek baru di Android Studio
Buka Android Studio dan buat proyek baru.
Pilih "Empty Compose Activity" sebagai template.
Beri nama proyek (misalnya: HappyBirthday).
Pilih bahasa "Kotlin" dan pastikan Minimum SDK adalah API 24 (Android 7.0) atau lebih tinggi.
Klik Finish untuk membuat proyek.

3. Mengatur Dependensi yang Dibutuhkan
Sebelum mulai menulis kode, pastikan Jetpack Compose telah didukung dalam proyek dengan memeriksa file build.gradle (Module: app). Jika belum ada, tambahkan dependensi berikut di dalam blok dependencies:

```
dependencies {
    implementation "androidx.activity:activity-compose:1.8.2"
    implementation "androidx.compose.ui:ui:1.6.1"
    implementation "androidx.compose.material3:material3:1.2.0"
}
```

3. Membuat dan Mengedit MainActivity.kt
Buka file MainActivity.kt yang berada dalam paket com.example.happybirthday, lalu hapus kode default yang ada. Gantilah dengan kode berikut:

package com.example.happybirthday

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.*
import androidx.compose.material3.*
import androidx.compose.runtime.Composable
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp


class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            BirthdayGreeting("Yasmin", "Love")
        }
    }
}

@Composable
fun BirthdayGreeting(name: String, from: String) {
    Column(
        modifier = Modifier.fillMaxSize(),
        verticalArrangement = Arrangement.Center,
        horizontalAlignment = Alignment.CenterHorizontally
    ) {
        Text(
            text = "Happy Birthday $name!",
            fontSize = 36.sp,
            fontWeight = FontWeight.Bold
        )
        Spacer(modifier = Modifier.height(16.dp))
        Text(
            text = "From $from",
            fontSize = 24.sp,
            color = Color.Red // Warna merah
        )
    }
}

4. Menjalankan Aplikasi
Setelah kode selesai ditulis, hubungkan perangkat Android atau jalankan Android Emulator. Klik tombol Run ▶ di Android Studio untuk mengeksekusi aplikasi. Jika berjalan dengan benar, layar akan menampilkan teks "Happy Birthday Yasmin!" dalam ukuran besar, serta teks "From Love" dalam warna merah. Dengan ini, aplikasi telah berhasil dibuat! 🎉

```
Happy Birthday Yasmin!
From Love
```


1.1 Aplikasi Happy Birthday


