# Week-9-Programming
Week 9 Programming Code

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
//Ryan Bain
//ITD-1253-60498
//11-9-2022

namespace Module9atinLayigPay
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void btnExit_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void btnReset_Click(object sender, EventArgs e)
        {
            textBox1.Text = "";
            label3.Text = "";
            textBox1.Focus();
        }

        private void btnPigLatin_Click(object sender, EventArgs e)
        {
            try
            {
                string word, piglatin;
                word = textBox1.Text;
                piglatin = word.Substring(1, word.Length - 1) + word.Substring(0, 1) + "ay";
                int c = 0;
                char[] word_1 = word.ToCharArray();
                for (int i = 0; i < word_1.Length; i++)
                {
                    if (!Char.IsLetterOrDigit(word_1[i]))
                    { c++; }
                    else if (c == word.Length)
                    {
                        label3.Text = "Don't just use special characters.";
                    }
                    else if (piglatin == word.Substring(1, word.Length - 1) + word.Substring(0, 1) + "ay")
                    {
                        label3.Text = piglatin;
                    }
                    }
                }
            catch (ArgumentOutOfRangeException)
            {
               
               label3.Text = "Please type something into the textbox.";
                

            }

        }


        private void lblPigLatinMessage_Click(object sender, EventArgs e)
        {

        }
    }
}
