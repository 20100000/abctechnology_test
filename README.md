<h1> Caso 1</h1>

Eu faria o redirecionmento no servidor de hopedagem. Ex: na opção domínios >> Redirecionamento 
no formulario de redirecionamento dominio utilizado e redireciona para outro dominio que escolher.

#Para fazer redirecionameto em PHP 
<pre>
header('Location: https://www.XPTO.com');
</pre>
#Para fazer em .htaccess
 RewriteEngine on
 RewriteCond %{HTTP_HOST} ^dominio-antigo.com.br$ [OR]<br>
 RewriteCond %{HTTP_HOST} ^www.XPTO.com$<br>
 RewriteRule ^(.*)$ http://www.dominio-novo.com.br/$1 [R=301,L]<br>

