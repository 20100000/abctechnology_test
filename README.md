<h1> Caso 1</h1>
Sera  necessário registrar o domínio gripe.com, o domínio deve apontar para IP do servidor, no servidor criar uma
 conta para esse domínio com cpanel. No cpanel na opção domínios >>  adicionar domínio acrescente o nome do domínio depois e subir o HTML para pasta public_html.
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
ou 
<pre>
    $headers = "Content-Type: text/plain; charset=utf-8";
    mail($email,$assunto,$msg,$headers)
</pre>
<h3>Em PHPMailer</h3>

<pre>
    $mail = new PHPMailer(); 
    $mail->charSet = "UTF-8";
</pre>

<h1> Caso 4</h1>

Versiona o código fonte no controlador de versão para retorna a versão anterior caso aja erro (dowgrade) .
Enviar nova versão para o repositório Master da aplicação  (pullRequest).<br>

.Uma forma para subir a aplicação, seria por FTP no servidor de hospedagem criar conta de FTP isso vai gerar<br> 
host <br>
usuário<br>
senha <br>

Outra forma fazer o upload da aplicação para o servidor de hospedagem em formato tipo zip para dentro do diretório <b>public_html</b>, em seguida descompactar a mesma.

Claro que antes necessário fazer teste para identifica erros nos ambientes de teste e de homologação
