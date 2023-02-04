# code

```
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Data.Sql;
using System.Data.SqlClient;
using System.IO;
using System.Data.Sql;
using System.Data.SqlClient;

namespace ImageUpload
{
    public partial class Form1 : Form
    {
        string extension = "";
        OpenFileDialog file;
     
        public Form1 ()
        {
            InitializeComponent();
        }

        private void button1_Click ( object sender, EventArgs e )
        {

            if (select.Text == "Save")
            {

                Random random = new Random();
                string number = random.Next().ToString();
                FileInfo fi = new FileInfo(file.FileName);
                extension = fi.Extension;
                int length = Application.StartupPath.Length - 9;
                string newPath = Application.StartupPath.Substring(0, length);
                string newImage = number + extension;
                pictureBox1.Image.Save(newPath + "image/" + newImage);

                string query = "INSERT INTO image values('"+ newImage+ "')";
                DB.db.Open();
                SqlCommand cmd = new SqlCommand(query,DB.db);
                cmd.ExecuteNonQuery();
                DB.db.Close();
                clearForm();
                MessageBox.Show("successfully uploaded");
            }
            else if (select.Text == "Select Image")
            {

                file = new OpenFileDialog();
                file.Filter = "Image Files(*.jpg; *.jpeg; *.png;)|*.jpg; *.jpeg; *.png;";
                file.ShowDialog();

                if (file.FileName != "")
                {

                    select.Text = "Save";
                    pictureBox1.Image = new Bitmap(file.FileName);
                }
            }
        }


        private void clearForm ()
        {
            pictureBox1.Image = null;
            select.Text = "Select Image";

        }

        private void button2_Click ( object sender, EventArgs e )
        {
            clearForm();
        }

        private void Form1_Load ( object sender, EventArgs e )
        {

        }
    }
}

```
