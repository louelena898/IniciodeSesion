# IniciodeSesion
C#, Microsoft Forms, Mono y Visual Studio Code


# INICIO DE SESION: 
//Nombre: Usuario 
//Password: 123

# CONCEPTO 1: Modificadores de Acceso (e.g., 'private', 'public')
Controlan la visibilidad y accesibilidad de miembros (campos, métodos, propiedades) dentro de una clase o entre clases.
 
private: El miembro solo es accesible desde dentro de la clase en la que está definido. Es ideal para encapsular la lógica interna y los datos, ocultándolos 
del mundo exterior. Ejemplo: private int miVariablePrivada;
 
public: El miembro es accesible desde cualquier lugar, dentro o fuera de la clase. Se usa para exponer la funcionalidad que otras partes de tu programa (o 
incluso otros programas) necesitan usar. Ejemplo: public void MiMetodoPublico();
 
Otros modificadores: protected, internal, protected internal, private protected.

# CONCEPTO 2: Tipo de Retorno 'void'
Indica que un método no devuelve ningún valor después de su ejecución. Los métodos 'void' se utilizan cuando la función principal del método es realizar una 
acción o un efecto secundario (mostrar algo en pantalla, guardar un archivo, etc.),  y no producir un resultado que necesite ser utilizado por quien lo llamó.

Ejemplo:
public void MostrarMensaje(string mensaje)
{
Console.WriteLine(mensaje); // Realiza una acción (imprime en consola)
}

# CONCEPTO 3: Manejadores de Eventos (Event Handlers)
Métodos especiales que se ejecutan en respuesta a un evento específico (e.g., un clic de botón, una pulsación de tecla). Siguen una firma estándar en .NET:
public void NombreMetodo(object sender, EventArgs e)

- object sender: Es una referencia al objeto que generó el evento, es eficzar para cuando múltiples controles comparten el mismo manejador de eventos y se 
necesita saber cuál de ellos lo activó.

- EventArgs e: Contiene datos específicos relacionados con el evento. 'EventArgs' es la clase base y se usa para eventos sin datos específicos. Para eventos 
más complejos (e.g., mouse, teclado), se usan clases derivadas (e.g., MouseEventArgs, KeyEventArgs) que contienen propiedades adicionales (posiciones del ratón, 
tecla presionada, etc.).
 
Ejemplo:
private void btnIniciarSesion_Click(object sender, EventArgs e)
 {
// Lógica que se ejecuta cuando el botón 'btnIniciarSesion' es clicado.
 }


# CONCEPTO 4: Clases y Objetos
Clase: Es un 'plano' o 'molde' para crear objetos. Define las propiedades (datos) y los métodos (comportamientos) que los objetos de ese tipo tendrán.
Ejemplo: public class LoginScreen : Form { ... } // LoginScreen es una clase
 
Objeto: Es una instancia concreta de una clase. Cuando creas un objeto, estás creando una entidad real basada en el plano de la clase.
Ejemplo: LoginScreen miVentanaLogin = new LoginScreen(); // miVentanaLogin es un objeto


# CONCEPTO 5: Windows Forms y su uso con Mono en Linux Mint
 Windows Forms (WinForms): Tecnología de Microsoft .NET para construir interfaces gráficas de usuario para aplicaciones de escritorio en Windows. Usa 
 los controles nativos de Windows.
 
 Mono: Implementación de código abierto del .NET Framework que permite ejecutar aplicaciones .NET en sistemas operativos no-Windows (como Linux y macOS). 
 Aunque puede ejecutar aplicaciones WinForms, no ofrece un diseñador visual nativo en Linux, lo que significa que el diseño de la interfaz se hace 
 programáticamente (escribiendo código para posicionar y configurar cada control).
 
Referencia a librerías: Para que el compilador de C# sepa dónde encontrar las definiciones de las clases  * de Windows Forms, se deben incluir referencias 
a las DLLs relevantes durante la compilación. Ejemplo: -r:System.Windows.Forms.dll -r:System.Drawing.dll
