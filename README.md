using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace CalculatorApp
{
    public partial class Calculator : Form
    {
        double firstNumber;
        string operation;
        public Calculator()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "1";
            }
            else
            {
                textBox.Text += "1";
            }
        }

        private void button2_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "2";
            }
            else
            {
                textBox.Text += "2";
            }
        }

        private void button3_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "3";
            }
            else
            {
                textBox.Text += "3";
            }
        }

        private void button4_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "4";
            }
            else
            {
                textBox.Text += "4";
            }
        }

        private void button5_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "5";
            }
            else
            {
                textBox.Text += "5";
            }
        }

        private void button6_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "6";
            }
            else
            {
                textBox.Text += "6";
            }
        }

        private void button7_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "7";
            }
            else
            {
                textBox.Text += "7";
            }
        }

        private void button8_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "8";
            }
            else
            {
                textBox.Text += "8";
            }
        }

        private void button9_Click(object sender, EventArgs e)
        {
            if (textBox.Text == "0" && textBox.Text != null)
            {
                textBox.Text = "9";
            }
            else
            {
                textBox.Text += "9";
            }
        }

        private void button0_Click(object sender, EventArgs e)
        {
              textBox.Text += "0";
            
        }

        private void add_button_Click(object sender, EventArgs e)
        {
            firstNumber = Convert.ToDouble(textBox.Text);
            textBox.Text = null;
            operation = "+";
        }

        private void sub_button_Click(object sender, EventArgs e)
        {
            firstNumber = Convert.ToDouble(textBox.Text);
            textBox.Text = null;
            operation = "-";
        }

        private void mul_button_Click(object sender, EventArgs e)
        {
            firstNumber = Convert.ToDouble(textBox.Text);
            textBox.Text = null;
            operation = "*";
        }

        private void div_button_Click(object sender, EventArgs e)
        {
            firstNumber = Convert.ToDouble(textBox.Text);
            textBox.Text = null;
            operation = "/";
        }

        private void eql_button_Click(object sender, EventArgs e)
        {
            double result, secondNumber;

            secondNumber = Convert.ToDouble(textBox.Text);

            if (operation == "+")
            {
                result = firstNumber + secondNumber;
                textBox.Text = Convert.ToString(result);
                firstNumber = result;
            }

            if (operation == "-")
            {
                result = firstNumber - secondNumber;
                textBox.Text = Convert.ToString(result);
                firstNumber = result;
            }

            if (operation == "*")
            {
                result = firstNumber * secondNumber;
                textBox.Text = Convert.ToString(result);
                firstNumber = result;
            }

            if (operation == "/")
            {
                if (secondNumber == 0)
                {
                    textBox.Text = "Sorry! Can't divide by zero.";
                }
                else{
                        result = firstNumber / secondNumber;
                        textBox.Text = Convert.ToString(result);
                        firstNumber = result;
                }
            }
        }

        private void dotbutton_Click(object sender, EventArgs e)
        {
            if(!textBox.Text.Contains("."))
            {
              textBox.Text += ".";
            }
        }

        private void C_button_Click(object sender, EventArgs e)
        {
            textBox.Text = null;
        }
    }
}
