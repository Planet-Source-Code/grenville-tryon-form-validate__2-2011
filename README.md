<div align="center">

## Form validate


</div>

### Description

This class was designed to send important information to clients via email with password,

Off-line connection on graphic mode. The same applet can be used to send a voucher, a greetings

card, a money confirmation of a transaction and so on. The source code is provided so, you can

customize as your needs (add music, change the encryption algorihtm, the logon window, etcs).

How to use the afp.class:

This is an applet that lets the user get information sended on an HTML encrypted page. To use,

the user must be try three times to enter a password (Encrypted into the HTML).

The special bonus is the facility of have a totally configurable information. Lets see the HTML:

HTML>

HEAD>TITLE>ESTADO DE CUENTA DE AFP HORIZONTE/TITLE>/HEAD>

BODY>

p align="center">

APPLET CODE="afp.class" WIDTH=640 HEIGHT=800>

PARAM NAME=Mensaje VALUE="KPSHF}Kpshf!ef!mb!Dsv{!Spkbt*256*161}2222222*643*161}Bw!3!ef!Nbzp*256*181}">

PARAM NAME=Titulo VALUE="010050NOMBRE DEL AFILIADO:|530025AFP HORIZONTE|490050CIUU:|010070DIRECCION:|220025ESTADO DE CUENTA DEL AFILIADO|015115SALDO A LA FECHA: 29/09/2,000|015205DETALLE DE MOVIMIENTOS AL 29/09/2000|015670OBSERVACIONES:|015595BONO DE RECONOCIMIENTO:|">

PARAM NAME=Pintar VALUE="005010620080000255255|005100620020000000255|005190620020000000255|005320620020000000255|005450620020000000255|005580620020000000255|005650620060000000255|">

PARAM NAME=Marco VALUE="001001630790|005010620080|005100620080|005100620020|005160620020|500100125080|005190620120|005190620020|500190125120|005320620120|005320620020|005320300120|005320400120|005320500120|005450620120|005450620020|005450300120|005450400120|005450500120|005580620060|005580620020|005580620040|200600200040|005650620120|005650620060|">

PARAM NAME=Imagenes VALUE="005010050030afplogo.gif|">

/APPLET>

/BODY>

Parameters on the HTML:

Titulo: (Title)

xxxyyyaaaaaaaaaaa|, where xxx is the x axis (3 digits), yyy is the y axis (3 digits),

aaaaaaa is the text to draw and | is the separators between distincts titles.

010050NOMBRE DEL AFILIADO| Will set the title NOMBRE DEL AFILIADO on 10,50 coors.

Pintar: (Fill)

xxxyyymmmnnnrrrgggbbb|, where xxx is the x1 axis (3 digits), yyy is the y1 axis (3 digits),

mmm is the x2 axis (3 digits), nnn is the y2 axis (3 digits), rrrgggbbb is the rgb color

and | is the separator between distincts fills.

005010620080000255255| Will fill a rectangle on (5,10,620,80) of rgb(0,255,255) color.

Marco: (Rectangle)

xxxyyymmmnnn|, where xxx is the x1 axis (3 digits), yyy is the y1 axis (3 digits),

mmm is the x2 axis (3 digits), nnn is the y2 axis (3 digits) and | is the separator between

distincts rectangles.

005010620080| Will draw a rectangle on (5,10,620,80), transparent background.

Imagenes: (Pictures)

xxxyyyaaaaa|, where xxx is the x axis (3 digits), yyy is the y axis (3 digits),

aaaaaaa is the image to draw (must be on the same folder where the class is) and | is the

separator betwen pictures.

005010050030afplogo.gif| Will draw the picture afplogo.gif in (5,10,50,30) coors.

Mensaje: (Messages)

aaaa}bbbbbb*xxx*yyy}, where aaaa is the password, } is the separator, bbbb is a message

with xxx as x axis and yyy as y axis. Each ASCII value will be rest on one (B=A,f=e...) to

get their real value.

KPSHF}Kpshf!ef!mb!Dsv{!Spkbt*256*161}, where:

KPSHF is the password (JORGE), and:

Kpshf!ef!mb!Dsv{!Spkbt*256*161 Will draw Jorge de la Cruz on (145,50) coors.
 
### More Info
 
The crypt method is, by far, simply. Just an idea of how to pass encrypted information via HTML.

Note that the image(s) must exists on the same dir.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Grenville Tryon](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/grenville-tryon.md)
**Level**          |Intermediate
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__2-68.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/grenville-tryon-form-validate__2-2011/archive/master.zip)

### API Declarations

<HTML>
<HEAD><TITLE>ESTADO DE CUENTA DE AFP HORIZONTE</TITLE></HEAD>
<BODY>
<p align="center">
<APPLET CODE="afp.class" WIDTH=640 HEIGHT=800>
<PARAM NAME=Mensaje VALUE="KPSHF}Kpshf!ef!mb!Dsv{!Spkbt*256*161}2222222*643*161}Bw!3!ef!Nbzp*256*181}">
<PARAM NAME=Titulo VALUE="010050NOMBRE DEL AFILIADO:|530025AFP HORIZONTE|490050CIUU:|010070DIRECCION:|220025ESTADO DE CUENTA DEL AFILIADO|015115SALDO A LA FECHA: 29/09/2,000|015205DETALLE DE MOVIMIENTOS AL 29/09/2000|015670OBSERVACIONES:|015595BONO DE RECONOCIMIENTO:|">
<PARAM NAME=Pintar VALUE="005010620080000255255|005100620020000000255|005190620020000000255|005320620020000000255|005450620020000000255|005580620020000000255|005650620060000000255|">
<PARAM NAME=Marco VALUE="001001630790|005010620080|005100620080|005100620020|005160620020|500100125080|005190620120|005190620020|500190125120|005320620120|005320620020|005320300120|005320400120|005320500120|005450620120|005450620020|005450300120|005450400120|005450500120|005580620060|005580620020|005580620040|200600200040|005650620120|005650620060|">
<PARAM NAME=Imagenes VALUE="005010050030afplogo.gif|">
</APPLET>
</BODY>


### Source Code

```
import java.awt.*;
import java.awt.event.*;
import java.awt.image.*;
public class afp extends java.applet.Applet {
TextField tf;
Button bo;
String[] Respuestas = new String [100];
String[] Titulos = new String [100];
String[] Marcos = new String [100];
String[] Pintas = new String [100];
String[] Imagenes = new String [100];
String Listo;
int Intentos;
//--------------------------------- inicio -------------------------------------------------------
public void init()
{
int i, Actual, CadaUno;
char CadaCaracter[], CaracterConvertido;
String Buffer, Mensaje,Marco,Pintar,Titulo,Imagen;
int x,y;
Listo="NO";
Intentos=0;
setBackground(Color.white);
setLayout(null);
tf = new TextField();
tf.setBounds( 220,60, 150, 25);
tf.setEchoChar('*');
add(tf);
bo = new Button("Aceptar");
bo.setBounds (420, 60, 80, 25);
add(bo);
//Arreglo de mensajes
Mensaje=getParameter("Mensaje");
if (Mensaje==null) Mensaje="?????";
CadaCaracter = new char [Mensaje.length()];
Mensaje.getChars(0,Mensaje.length(),CadaCaracter,0);
Buffer="";
Actual=0;
for (i=0;i<Mensaje.length();i++)
 {
 CadaUno= (int) CadaCaracter[i];
 CadaUno--;
 CaracterConvertido = (char) CadaUno;
 if (CadaUno == 124)
 {
 Respuestas[Actual]=Buffer;
 Actual++;
 Buffer="";
 }
 else
 {Buffer += CaracterConvertido;};
 };
//Arreglo de titulos
Titulo=getParameter("Titulo");
if (Titulo==null) Titulo="";
CadaCaracter = new char [Titulo.length()];
Titulo.getChars(0,Titulo.length(),CadaCaracter,0);
Buffer="";
Actual=0;
for (i=0;i<Titulo.length();i++)
 {
 CadaUno= (int) CadaCaracter[i];
 CaracterConvertido = (char) CadaUno;
 if (CadaUno == 124)
 {
 Titulos[Actual]=Buffer;
 Actual++;
 Buffer="";
 }
 else
 {Buffer += CaracterConvertido;};
 };
//Arreglo de imagenes
Imagen=getParameter("Imagenes");
if (Imagen==null) Imagen="";
CadaCaracter = new char [Imagen.length()];
Imagen.getChars(0,Imagen.length(),CadaCaracter,0);
Buffer="";
Actual=0;
for (i=0;i<Imagen.length();i++)
 {
 CadaUno= (int) CadaCaracter[i];
 CaracterConvertido = (char) CadaUno;
 if (CadaUno == 124)
 {
 Imagenes[Actual]=Buffer;
 Actual++;
 Buffer="";
 }
 else
 {Buffer += CaracterConvertido;};
 };
//Arreglo de Marcos
Marco=getParameter("Marco");
if (Marco == null) Marco="";
CadaCaracter = new char [Marco.length()];
Marco.getChars(0,Marco.length(),CadaCaracter,0);
Buffer="";
Actual=0;
for (i=0;i<Marco.length();i++)
 {
 CaracterConvertido = CadaCaracter[i];
 if (CaracterConvertido == '|')
 {
 Marcos[Actual]=Buffer;
 Actual++;
 Buffer="";
 }
 else
 {Buffer += CaracterConvertido;};
 };
//Arreglo de Pintados
Pintar=getParameter("Pintar");
if (Pintar == null) Pintar="";
CadaCaracter = new char [Pintar.length()];
Pintar.getChars(0,Pintar.length(),CadaCaracter,0);
Buffer="";
Actual=0;
for (i=0;i<Pintar.length();i++)
 {
 CaracterConvertido = CadaCaracter[i];
 if (CaracterConvertido == '|')
 {
 Pintas[Actual]=Buffer;
 Actual++;
 Buffer="";
 }
 else
 {Buffer += CaracterConvertido;};
 };
tf.requestFocus();
}
//--------------------------------- VALORES -------------------------------------------------------
public String RetornaValor(int Valor)
{return Respuestas[Valor];}
//--------------------------------- PINTADO -------------------------------------------------------
public void Pintado(Graphics g)
{
int i,j,Actual,x,y;
char CadaUno,CaracterConvertido,CadaCaracter[],limite=')';
String Buffer,Cadena,Mensaje;
String x1,y1,x2,y2,rr,gg,bb;
Toolkit tk = Toolkit.getDefaultToolkit();
//fondo blanco para applet
 g.setColor(new Color(255,255,255));
 g.fillRect(0,0,630,790);
//color negro (en adelante)
 g.setColor(new Color(0,0,0));
//marco general
{
 g.setColor(new Color(255,255,255));
 g.fillRect(0,0,630,790);
 g.setColor(new Color(0,0,0));
// Pintar
for (i=0;i<100;i++)
{
if (Pintas[i]==null) Pintas[i]="";
if (Pintas[i].length()>0)
{
Buffer=Pintas[i];
x1= Buffer.substring(0,3);
y1= Buffer.substring(3,6);
x2= Buffer.substring(6,9);
y2= Buffer.substring(9,12);
rr= Buffer.substring(12,15);
gg= Buffer.substring(15,18);
bb= Buffer.substring(18,21);
g.setColor(new Color(Integer.parseInt(rr),Integer.parseInt(gg),Integer.parseInt(bb)));
g.fillRect(Integer.parseInt(x1),Integer.parseInt(y1),Integer.parseInt(x2),Integer.parseInt(y2));
g.setColor(new Color(0,0,0));
};
};
// Marcos
for (i=0;i<100;i++)
{
if (Marcos[i]==null) Marcos[i]="";
if (Marcos[i].length()>0)
{
Buffer=Marcos[i];
x1= Buffer.substring(0,3);
y1= Buffer.substring(3,6);
x2= Buffer.substring(6,9);
y2= Buffer.substring(9,12);
g.drawRect(Integer.parseInt(x1),Integer.parseInt(y1),Integer.parseInt(x2),Integer.parseInt(y2));
};
};
//IMAGENES
for (j=0;j<100;j++)
{
 Mensaje=Imagenes[j];
 if (Mensaje==null) Mensaje="";
 if (Mensaje.length()>12) g.drawImage(getImage(getCodeBase(),Mensaje.substring(12)),Integer.parseInt(Mensaje.substring(0,3)),Integer.parseInt(Mensaje.substring(3,6)),Integer.parseInt(Mensaje.substring(6,9)),Integer.parseInt(Mensaje.substring(9,12)),this);
};
//TITULOS
g.setColor(new Color(0,0,0));
g.setFont(new Font("Arial",Font.BOLD,12));
for (j=0;j<100;j++)
{
 Mensaje=Titulos[j];
 if (Mensaje==null) Mensaje="";
 if (Mensaje.length()>6) g.drawString(Mensaje.substring(6),Integer.parseInt(Mensaje.substring(0,3)),Integer.parseInt(Mensaje.substring(3,6)));
};
//texto desencriptado
g.setColor(new Color(0,0,128));
g.setFont(new Font("Arial",Font.BOLD,12));
for (j=1;j<100;j++)
{
 Cadena="";
 x=0;
 y=0;
 Mensaje=Respuestas[j];
 CadaCaracter = new char [Mensaje.length()];
 Mensaje.getChars(0,Mensaje.length(),CadaCaracter,0);
 Buffer="";
 Actual=0;
 for (i=0;i<Mensaje.length();i++)
 {
 if (CadaCaracter[i] == limite)
 {
 if (Actual==0) {Cadena=Buffer;};
 if (Actual==1) {x= Integer.parseInt(Buffer);};
 Buffer="";
 Actual++;
 }
 else
 {Buffer += CadaCaracter[i];};
 }
 y= Integer.parseInt(Buffer);
 g.drawString(Cadena,x,y);
}
}
}
//--------------------------------- PINTADO -------------------------------------------------------
public void paint(Graphics g)
{
if (Listo=="SI")
{
Pintado(g);
showStatus("AFP Horizonte");
}
if (Listo=="NO")
{
g.setFont(new Font("Arial",Font.BOLD,24));
g.drawString("AFP HORIZONTE",0,40);
g.setFont(new Font("Arial",Font.PLAIN,12));
g.drawString("INGRESE SU CLAVE SECRETA:",0,80);
if (Intentos == 0) showStatus("AFP HORIZONTE");
if (Intentos == 3)
 {g.setFont(new Font("Arial",Font.PLAIN,12));
 g.setColor(new Color(255,255,255));
 g.drawString("INGRESE SU CLAVE SECRETA:",0,80);
 g.setFont(new Font("Arial",Font.BOLD,24));
 g.setColor(new Color(255,0,0));
 g.drawString("Su clave es errada. Comuniquese con el 221-2363.",0,160);
 showStatus("AFP HORIZONTE");
 }
}
}
//--------------------------------- ADMINISTRADOR DE EVENTOS -------------------------------------------------------
public boolean action(Event evt,Object what)
{
String Cadena;
String Compara;
if (evt.target instanceof Button)
{Cadena=tf.getText();
 Compara=Respuestas[0];
 if (Cadena.equals(Compara))
 {Listo="SI";
 bo.setVisible(false);
 tf.setVisible(false);
 }
 else
 {
 tf.setSelectionStart(0);
 tf.setSelectionEnd(tf.getText().length());
 tf.requestFocus();
 Intentos++;
 showStatus("Intentos:"+String.valueOf(Intentos)+" de 3.");
 if (Intentos==3)
 {bo.setVisible(false);
 tf.setVisible(false);
 };
 };
};
repaint();
return true;
}
}
```

