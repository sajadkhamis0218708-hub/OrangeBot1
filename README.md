package com.orangebot.app

import android.app.Activity
import android.os.Bundle
import android.graphics.Color
import android.view.Gravity
import android.widget.Button
import android.widget.LinearLayout
import android.widget.TextView

class MainActivity : Activity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        val layout = LinearLayout(this)
        layout.orientation = LinearLayout.VERTICAL
        layout.gravity = Gravity.CENTER
        layout.setPadding(30, 30, 30, 30)

        val title = TextView(this)
        title.text = "Orange Bot"
        title.textSize = 28f
        title.gravity = Gravity.CENTER

        val status = TextView(this)
        status.text = "ربات آماده است"
        status.textSize = 20f
        status.gravity = Gravity.CENTER

        val start = Button(this)
        start.text = "شروع ربات"

        val stop = Button(this)
        stop.text = "توقف ربات"

        start.setOnClickListener {
            status.text = "ربات روشن شد"
