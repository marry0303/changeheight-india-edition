package com.world1.yuto.changeheight;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Button;
import android.widget.Toast;

import static com.world1.yuto.changeheight.R.id.editText10;
import static com.world1.yuto.changeheight.R.id.editText12;
/**
 * Created by machidukuri306_1 on 2016/11/14.
 */
public class imperial extends MainActivity{
    @Override
public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.imperial);
    
        Button b1 = (Button) findViewById(R.id.button17);
        b1.setOnClickListener(new View.OnClickListener() {
            public void onClick(View v) {
                Intent intent = new Intent(imperial.this, MainActivity.class);
                intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
                intent.addFlags(Intent.FLAG_ACTIVITY_SINGLE_TOP);
                startActivity(intent);
            }
        });}

    public void button15_click(View view){
        EditText editText1 = (EditText) findViewById(editText10);
        String A = editText1.getText().toString().trim();
        if (A.equals("")){
            Toast.makeText(
                    this,
                    "Please enter your height",
                    Toast.LENGTH_LONG
            ).show();return;}
        int a = Integer.parseInt(A);
        if(a>9 || a<0){Toast.makeText(
                this,
                "You can enter from 0ft to 9ft!",
                Toast.LENGTH_LONG
        ).show();}

        EditText editText11 = (EditText) findViewById(editText12);
        String AA = editText11.getText().toString().trim();
        if (AA.equals("")){
            Toast.makeText(
                    this,
                    "Please enter your height",
                    Toast.LENGTH_LONG
            ).show();return;}
        int aa = Integer.parseInt(AA);
        if(aa>11 || aa<0){Toast.makeText(
                this,
                "You can enter from 1in to 11in!",
                Toast.LENGTH_LONG
        ).show();}
        else {
            int b = a*12;
            int c = aa+b;
            double d=c/1.084265964450296;
            int e =(int) Math.round(d);
            int f=e/12;int g=e%12;
            TextView textView10 = (TextView) findViewById(R.id.textView10);
            String s = String.valueOf(f);
            String t = String.valueOf(g);
            textView10.setText(String.valueOf("If you are girl,you are "+ s +"ft"+ t +"in"));
        }
    }

    public void button16_click(View view){
        EditText editText1 = (EditText) findViewById(editText10);
        String A = editText1.getText().toString().trim();
        if (A.equals("")){
            Toast.makeText(
                    this,
                    "Please enter your height",
                    Toast.LENGTH_LONG
            ).show();return;}
        int a = Integer.parseInt(A);
        if(a>9 || a<0){Toast.makeText(
                this,
                "You can enter from 0ft to 9ft!",
                Toast.LENGTH_LONG
        ).show();}

        EditText editText11 = (EditText) findViewById(editText12);
        String AA = editText11.getText().toString().trim();
        if (AA.equals("")){
            Toast.makeText(
                    this,
                    "Please enter your height",
                    Toast.LENGTH_LONG
            ).show();return;}
        int aa = Integer.parseInt(AA);
        if(aa>11 || aa<0){Toast.makeText(
                this,
                "You can enter from 1in to 11in!",
                Toast.LENGTH_LONG
        ).show();}
        else {
            int b = a*12;
            int c = aa+b;
            double d=c*1.084265964450296;
            int e =(int) Math.round(d);
            int f=e/12;int g=e%12;
            TextView textView10 = (TextView) findViewById(R.id.textView10);
            String s = String.valueOf(f);
            String t = String.valueOf(g);
            textView10.setText(String.valueOf("If you are boy,you are "+ s +"ft"+ t +"in"));
        }
    }
    }
