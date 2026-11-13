package com.gptoxide.v2

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.background
import androidx.compose.foundation.layout.*
import androidx.compose.foundation.shape.RoundedCornerShape
import androidx.compose.material3.*
import androidx.compose.runtime.*
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp

private val Purple = Color(0xFF8B45FF)
private val Dark = Color(0xFF100D19)

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            OxideApp()
        }
    }
}

@Composable
fun OxideApp() {
    var esp by remember { mutableStateOf(false) }
    var aim by remember { mutableStateOf(false) }
    var fps by remember { mutableStateOf(true) }
    var dark by remember { mutableStateOf(true) }

    MaterialTheme {
        Column(
            modifier = Modifier
                .fillMaxSize()
                .background(Dark)
                .padding(20.dp),
            horizontalAlignment = Alignment.CenterHorizontally
        ) {
            Spacer(Modifier.height(25.dp))

            Text(
                "GPT OXIDE V2",
                color = Purple,
                fontSize = 30.sp
            )

            Text(
                "ANDROID EDITION",
                color = Color.Gray,
                fontSize = 12.sp
            )

            Spacer(Modifier.height(30.dp))

            SettingItem("Показывать FPS", fps) { fps = it }
            SettingItem("Тёмная тема", dark) { dark = it }

            Spacer(Modifier.height(20.dp))

            Text(
                "НАСТРОЙКИ ИНТЕРФЕЙСА",
                color = Purple,
                fontSize = 16.sp
            )

            SettingItem("Анимации меню", esp) { esp = it }
            SettingItem("Плавающая панель", aim) { aim = it }

            Spacer(Modifier.height(30.dp))

            Button(
                onClick = {
                    esp = false
                    aim = false
                    fps = true
                    dark = true
                },
                colors = ButtonDefaults.buttonColors(
                    containerColor = Purple
                ),
                modifier = Modifier.fillMaxWidth()
            ) {
                Text("СБРОСИТЬ НАСТРОЙКИ")
            }

            Spacer(Modifier.weight(1f))

            Text(
                "GPT OXIDE V2 • 2026",
                color = Color.Gray,
                fontSize = 11.sp
            )
        }
    }
}

@Composable
fun SettingItem(
    title: String,
    checked: Boolean,
    onChange: (Boolean) -> Unit
) {
    Row(
        modifier = Modifier
            .fillMaxWidth()
            .padding(vertical = 10.dp)
            .background(
                Color(0xFF211B30),
                RoundedCornerShape(14.dp)
            )
            .padding(15.dp),
        verticalAlignment = Alignment.CenterVertically
    ) {
        Text(
            title,
            color = Color.White,
            modifier = Modifier.weight(1f)
        )

        Switch(
            checked = checked,
            onCheckedChange = onChange
        )
    }
}
