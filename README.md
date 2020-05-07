<h1> Caso 1</h1>

Eu faria o redirecionmento no servidor de hopedagem. <br>
<h3>Para servidor de hospedagem</h3>
Ex: na opção domínios >> Redirecionamento 
no formulario de redirecionamento dominio utilizado e redireciona para outro dominio que escolher.

<h3>Para fazer redirecionameto em PHP</h3> 
<pre>
header('Location: https://www.XPTO.com');
</pre>
<h3>Para fazer em .htaccess</h3>
 RewriteEngine on
 RewriteCond %{HTTP_HOST} ^dominio-antigo.com.br$ [OR]<br>
 RewriteCond %{HTTP_HOST} ^www.XPTO.com$<br>
 RewriteRule ^(.*)$ http://www.dominio-novo.com.br/$1 [R=301,L]<br>

<h1> Caso 2</h1>
<h1> Caso 3</h1>
   Definir padrão do charset para utf-8
<h3>Em HTML</h3>
<pre>
    meta charset="utf-8"
</pre>
<h3>Em PHP</h3>
<pre>
    header("Content-type: text/html; charset=utf-8");
</pre>
<h3>Em PHPMailer</h3>

<pre>
    $mail = new PHPMailer(); 
    $mail->charSet = "UTF-8";
</pre>

<h1> Caso 4</h1>
