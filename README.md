<h1> Caso 1</h1>

Eu faria o redirecionmento no servidor de hopedagem. Ex: na opção domínios >> Redirecionamento 
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

