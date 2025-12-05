"1
    // Muestra el nombre en pantalla
    Console.WriteLine("¡Hola, " + nombre + "! Bienvenido al programa.");

    // Espera a que el usuario presione una tecla antes de cerrar
    Console.WriteLine("Presiona cualquier tecla para salir...");
    Console.ReadKey();
}


#2
    Console.ForegroundColor = ConsoleColor.Red;


    Console.Write("Por favor, escribe tu nombre: ");
    string nombre = Console.ReadLine();


    Console.Write("ingresa tu edad ");
    int edad = Console.ReadLine();

    Console.WriteLine("❤ ¡Hola, " + nombre + edad + "! ❤");


    Console.ResetColor();


    Console.WriteLine("Presiona cualquier tecla para salir...");
    Console.ReadKey();
}

#3
    Console.Write("Ingrese el segundo número: ");
    int b = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el tercer número: ");
    int c = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el cuarto número: ");
    int d = int.Parse(Console.ReadLine());

    // Operaciones
    int suma = a + b + c + d;
    int resta = a - b - c - d;
    int multiplicacion = a * b * c * d;
    int modulo = a % b; // Ejemplo usando solo dos variables

    // Resultados
    Console.WriteLine("\nRESULTADOS:");
    Console.WriteLine("Suma: " + suma);
    Console.WriteLine("Resta: " + resta);
    Console.WriteLine("Multiplicación: " + multiplicacion);
    Console.WriteLine("Módulo (a % b): " + modulo);

    Console.WriteLine("\nPresione una tecla para salir...");
    Console.ReadKey();
}
#4
    Console.Write("Ingrese el primer número: ");
    int a = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el segundo número: ");
    int b = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el tercer número: ");
    int c = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el cuarto número: ");
    int d = int.Parse(Console.ReadLine());

    
    int suma = a + b + c + d;
    int resta = a - b - c - d;
    int multiplicacion = a * b * c * d;
    int modulo = a % b; 

    
    Console.WriteLine("\nRESULTADOS:");
    Console.WriteLine("Suma: " + suma);
    Console.WriteLine("Resta: " + resta);
    Console.WriteLine("Multiplicación: " + multiplicacion);
    Console.WriteLine("Módulo (a % b): " + modulo);

    Console.WriteLine("\nPresione una tecla para salir...");
    Console.ReadKey();
}
#5
    Console.Write("Ingrese el primer numero: ");
    int a = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el segundo numero: ");
    int b = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el tercer numero: ");
    int c = int.Parse(Console.ReadLine());

    Console.Write("Ingrese el cuarto numero: ");
    int d = int.Parse(Console.ReadLine());

    
    int suma = a + b + c + d;
    int resta = a - b - c - d;
    int multiplicacion = a * b * c * d;
    int modulo = a % b; 

    
    Console.WriteLine("\nRESULTADOS:");
    Console.WriteLine("Suma: " + suma);
    Console.WriteLine("Resta: " + resta);
    Console.WriteLine("Multiplicacion: " + multiplicacion);
    Console.WriteLine("Modulo (a % b): " + modulo);

    Console.WriteLine("\nPresione una tecla para salir...");
    Console.ReadKey();
}
#6
// Constructor
public Rectangulo(double baseRect, double altura)
{
    this.baseRect = baseRect;
    this.altura = altura;
}

// Método para calcular el área
public double CalcularArea()
{
    return baseRect * altura;
}

// Método para calcular el perímetro
public double CalcularPerimetro()
{
    return 2 * (baseRect + altura);
}
#7
    // Imprimir en consola el área y el perímetro
    Console.WriteLine("Área del rectángulo: " + r.CalcularArea());
    Console.WriteLine("Perímetro del rectángulo: " + r.CalcularPerimetro());
}
#8
using System;

Console.WriteLine("Ingresa un número del 1 al 7 para elegir un día de la semana:"); string input = Console.ReadLine();

if (int.TryParse(input, out int day)) { switch (day) { case 1: Console.WriteLine("Monday"); break; case 2: Console.WriteLine("Tuesday"); break; case 3: Console.WriteLine("Wednesday"); break; case 4: Console.WriteLine("Thursday"); break; case 5: Console.WriteLine("Friday"); break; case 6: Console.WriteLine("Saturday"); break; case 7: Console.WriteLine("Sunday"); break; default: Console.WriteLine("Número fuera de rango. Debe ser entre 1 y 7."); break; } } else { Console.WriteLine("Entrada inválida. Debes ingresar un número."); }

using System;

Console.WriteLine("Ingresa un número del 1 al 7 para elegir un día de la semana:"); int day = int.Parse(Console.ReadLine());

switch (day) { case 1: Console.WriteLine("Monday"); break; case 2: Console.WriteLine("Tuesday"); break; case 3: Console.WriteLine("Wednesday"); break; case 4: Console.WriteLine("Thursday"); break; case 5: Console.WriteLine("Friday"); break; case 6: Console.WriteLine("Saturday"); break; case 7: Console.WriteLine("Sunday"); break; default: Console.WriteLine("Número fuera de rango. Debe ser entre 1 y 7."); break; }

int anotherDay = 4;

switch (anotherDay) { case 6: Console.WriteLine("Today is Saturday"); break;

case 7:
    Console.WriteLine("Today is Sunday");
    break;

default:
    Console.WriteLine("Looking forward to the Weekend");
    break;

}
#9
using System; using System.Windows.Forms;

namespace MenuSwitchApp { public partial class FormMenu : Form { public FormMenu() { InitializeComponent(); }

    private void btnConsultar_Click(object sender, EventArgs e)
    {
        int opcion;
        bool valido = int.TryParse(txtNumero.Text, out opcion);

        if (!valido)
        {
            lblResultado.Text = "Ingrese un número válido.";
            return;
        }

        switch (opcion)
        {
            case 1:
                lblResultado.Text = "Hamburguesa Doble + Papas ($5.00)";
                break;

            case 2:
                lblResultado.Text = "Pizza Personal + Soda ($4.50)";
                break;

            case 3:
                lblResultado.Text = "Ensalada César + Agua ($6.00)";
                break;

            case 4:
                lblResultado.Text = "Nuggets x10 + Jugo ($4.00)";
                break;

            default:
                lblResultado.Text = "Combo NO existente. Intente de nuevo.";
                break;
        }
    }
}

}
#10
using System; using System.Windows.Forms;

namespace MenuSwitchApp { static class Program { [STAThread] static void Main() { Application.EnableVisualStyles(); Application.SetCompatibleTextRenderingDefault(false); Application.Run(new FormMenu()); } } }

namespace MenuSwitchApp { partial class FormMenu { private System.ComponentModel.IContainer components = null; private System.Windows.Forms.Label lblTitulo; private System.Windows.Forms.Label lblInstruccion; private System.Windows.Forms.TextBox txtNumero; private System.Windows.Forms.Button btnConsultar; private System.Windows.Forms.Label lblResultado;

    protected override void Dispose(bool disposing)
    {
        if (disposing && (components != null))
        {
            components.Dispose();
        }
        base.Dispose(disposing);
    }

    private void InitializeComponent()
    {
        this.lblTitulo = new System.Windows.Forms.Label();
        this.lblInstruccion = new System.Windows.Forms.Label();
        this.txtNumero = new System.Windows.Forms.TextBox();
        this.btnConsultar = new System.Windows.Forms.Button();
        this.lblResultado = new System.Windows.Forms.Label();
        this.SuspendLayout();
        // 
        // lblTitulo
        // 
        this.lblTitulo.AutoSize = true;
        this.lblTitulo.Font = new System.Drawing.Font("Segoe UI", 18F);
        this.lblTitulo.Location = new System.Drawing.Point(90, 20);
        this.lblTitulo.Text = "Menú del Día";
        // 
        // lblInstruccion
        // 
        this.lblInstruccion.AutoSize = true;
        this.lblInstruccion.Location = new System.Drawing.Point(40, 80);
        this.lblInstruccion.Text = "Ingrese el número de combo (1-4):";
        // 
        // txtNumero
        // 
        this.txtNumero.Location = new System.Drawing.Point(250, 78);
        this.txtNumero.Width = 50;
        // 
        // btnConsultar
        // 
        this.btnConsultar.Location = new System.Drawing.Point(130, 130);
        this.btnConsultar.Text = "Ver Detalles";
        this.btnConsultar.Click += new System.EventHandler(this.btnConsultar_Click);
        // 
        // lblResultado
        // 
        this.lblResultado.BorderStyle = System.Windows.Forms.BorderStyle.Fixed3D;
        this.lblResultado.Font = new System.Drawing.Font("Segoe UI", 14F);
        this.lblResultado.Location = new System.Drawing.Point(40, 200);
        this.lblResultado.Size = new System.Drawing.Size(300, 40);
        this.lblResultado.Text = "---";
        // 
        // FormMenu
        // 
        this.ClientSize = new System.Drawing.Size(380, 300);
        this.Controls.Add(this.lblTitulo);
        this.Controls.Add(this.lblInstruccion);
        this.Controls.Add(this.txtNumero);
        this.Controls.Add(this.btnConsultar);
        this.Controls.Add(this.lblResultado);
        this.Name = "FormMenu";
        this.Text = "Selector de Menú";
        this.ResumeLayout(false);
        this.PerformLayout();
    }
}

}

#11
using System; using System.Windows.Forms;

namespace MenuSwitchApp { static class Program { [STAThread] static void Main() { Application.EnableVisualStyles(); Application.SetCompatibleTextRenderingDefault(false); Application.Run(new FormMenu()); } } }

using System; using System.Windows.Forms;

namespace MenuSwitchApp { public partial class FormMenu : Form { public FormMenu() { InitializeComponent(); }

    private void btnConsultar_Click(object sender, EventArgs e)
    {
        int opcion;
        bool valido = int.TryParse(txtNumero.Text, out opcion);

        if (!valido)
        {
            lblResultado.Text = "Ingrese un número válido.";
            return;
        }

        switch (opcion)
        {
            case 1:
                lblResultado.Text = "Hamburguesa Doble + Papas ($5.00)";
                break;
            case 2:
                lblResultado.Text = "Pizza Personal + Soda ($4.50)";
                break;
            case 3:
                lblResultado.Text = "Ensalada César + Agua ($6.00)";
                break;
            case 4:
                lblResultado.Text = "Nuggets x10 + Jugo ($4.00)";
                break;
            default:
                lblResultado.Text = "Combo NO existente. Intente de nuevo.";
                break;
        }
    }

    private void btnVerTodos_Click(object sender, EventArgs e)
    {
        FormListaCombos ventana = new FormListaCombos();
        ventana.ShowDialog();
    }
}

}

namespace MenuSwitchApp { partial class FormMenu { private System.ComponentModel.IContainer components = null; private System.Windows.Forms.Label lblTitulo; private System.Windows.Forms.Label lblInstruccion; private System.Windows.Forms.TextBox txtNumero; private System.Windows.Forms.Button btnConsultar; private System.Windows.Forms.Label lblResultado; private System.Windows.Forms.Button btnVerTodos;

    protected override void Dispose(bool disposing)
    {
        if (disposing && (components != null))
        {
            components.Dispose();
        }
        base.Dispose(disposing);
    }

    private void InitializeComponent()
    {
        this.lblTitulo = new System.Windows.Forms.Label();
        this.lblInstruccion = new System.Windows.Forms.Label();
        this.txtNumero = new System.Windows.Forms.TextBox();
        this.btnConsultar = new System.Windows.Forms.Button();
        this.lblResultado = new System.Windows.Forms.Label();
        this.btnVerTodos = new System.Windows.Forms.Button();
        this.SuspendLayout();
        // 
        // lblTitulo
        // 
        this.lblTitulo.AutoSize = true;
        this.lblTitulo.Font = new System.Drawing.Font("Segoe UI", 18F);
        this.lblTitulo.Location = new System.Drawing.Point(90, 20);
        this.lblTitulo.Text = "Menú del Día";
        // 
        // lblInstruccion
        // 
        this.lblInstruccion.AutoSize = true;
        this.lblInstruccion.Location = new System.Drawing.Point(40, 80);
        this.lblInstruccion.Text = "Ingrese el número de combo (1-4):";
        // 
        // txtNumero
        // 
        this.txtNumero.Location = new System.Drawing.Point(250, 78);
        this.txtNumero.Width = 50;
        // 
        // btnConsultar
        // 
        this.btnConsultar.Location = new System.Drawing.Point(130, 130);
        this.btnConsultar.Text = "Ver Detalles";
        this.btnConsultar.Click += new System.EventHandler(this.btnConsultar_Click);
        // 
        // lblResultado
        // 
        this.lblResultado.BorderStyle = System.Windows.Forms.BorderStyle.Fixed3D;
        this.lblResultado.Font = new System.Drawing.Font("Segoe UI", 14F);
        this.lblResultado.Location = new System.Drawing.Point(40, 200);
        this.lblResultado.Size = new System.Drawing.Size(300, 40);
        this.lblResultado.Text = "---";
        // 
        // btnVerTodos
        // 
        this.btnVerTodos.Location = new System.Drawing.Point(110, 260);
        this.btnVerTodos.Text = "Ver Todos los Combos";
        this.btnVerTodos.Click += new System.EventHandler(this.btnVerTodos_Click);
        // 
        // FormMenu
        // 
        this.ClientSize = new System.Drawing.Size(380, 330);
        this.Controls.Add(this.lblTitulo);
        this.Controls.Add(this.lblInstruccion);
        this.Controls.Add(this.txtNumero);
        this.Controls.Add(this.btnConsultar);
        this.Controls.Add(this.lblResultado);
        this.Controls.Add(this.btnVerTodos);
        this.Name = "FormMenu";
        this.Text = "Selector de Menú";
        this.ResumeLayout(false);
        this.PerformLayout();
    }
}

}

using System; using System.Windows.Forms;

namespace MenuSwitchApp { public partial class FormListaCombos : Form { public FormListaCombos() { InitializeComponent();

        lblCombos.Text =
            "1. Hamburguesa Doble + Papas ($5.00)\n" +
            "2. Pizza Personal + Soda ($4.50)\n" +
            "3. Ensalada César + Agua ($6.00)\n" +
            "4. Nuggets x10 + Jugo ($4.00)\n";
    }
}

}

namespace MenuSwitchApp { partial class FormListaCombos { private System.ComponentModel.IContainer components = null; private System.Windows.Forms.Label lblTitulo; private System.Windows.Forms.Label lblCombos;

    protected override void Dispose(bool disposing)
    {
        if (disposing && (components != null))
        {
            components.Dispose();
        }
        base.Dispose(disposing);
    }

    private void InitializeComponent()
    {
        this.lblTitulo = new System.Windows.Forms.Label();
        this.lblCombos = new System.Windows.Forms.Label();
        this.SuspendLayout();
        // 
        // lblTitulo
        // 
        this.lblTitulo.AutoSize = true;
        this.lblTitulo.Font = new System.Drawing.Font("Segoe UI", 16F);
        this.lblTitulo.Location = new System.Drawing.Point(40, 20);
        this.lblTitulo.Text = "Lista de Combos Disponibles";
        // 
        // lblCombos
        // 
        this.lblCombos.BorderStyle = System.Windows.Forms.BorderStyle.Fixed3D;
        this.lblCombos.Font = new System.Drawing.Font("Segoe UI", 12F);
        this.lblCombos.Location = new System.Drawing.Point(20, 80);
        this.lblCombos.Size = new System.Drawing.Size(330, 200);
        this.lblCombos.Text = "---";
        // 
        // FormListaCombos
        // 
        this.ClientSize = new System.Drawing.Size(380, 320);
        this.Controls.Add(this.lblTitulo);
        this.Controls.Add(this.lblCombos);
        this.Name = "FormListaCombos";
        this.Text = "Lista de Combos";
        this.ResumeLayout(false);
        this.PerformLayout();
    }
}

}

class Car { private string model = "Mustang";

static void Main(string[] args) { Car myObj = new Car(); Console.WriteLine(myObj.model); } }

class Person { private string name; // field public string Name // property { get { return name; } set { name = value; } } }

class Program { static void Main(string[] args) { Person myObj = new Person(); myObj.Name = "Liam"; Console.WriteLine(myObj.Name); } }****
