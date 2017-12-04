# From Udemy..problem with View.getId()

package com.adriano.conversomoedas;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity implements View.OnClickListener {


    private ViewHolder mViewHolder = new ViewHolder();

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        this.mViewHolder.editValue = findViewById(R.id.edit_value);
        this.mViewHolder.textDollar = findViewById(R.id.text_dollar);
        this.mViewHolder.textEuro = findViewById(R.id.text_euro);
        this.mViewHolder.buttonCalculate = findViewById(R.id.button_calculate);

        this.mViewHolder.buttonCalculate.setOnClickListener(this);
    }

    @Override
        //Busca os elementos da interface
    public void onClick(View view) {
        int id = View.getId();
        if (id == R.id.button_calculate) {
        this.mViewHolder.buttonCalculate.setText("Teste");
        }
    }

    private static class ViewHolder {
        EditText editValue;
        TextView textDollar;
        TextView textEuro;
        Button buttonCalculate;


    }
}
