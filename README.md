<h1> Caso 1</h1>
Sera  necessário registrar o domínio gripe.com, o domínio deve apontar para IP do servidor, no servidor criar uma
 conta para esse domínio com cpanel. No cpanel na opção domínios >>  adicionar domínio acrescente o nome do domínio depois e subir o HTML para pasta public_html.
<h1> Caso 2</h1>
Acredito que devemos pegar ami do snapshop do ultimo dia do ano de 2019. Criar um novo volume ou seja um novo disco e anexa no servidor  para receber a copia do disco 2019.
com o volume pronto rode comandos exemplo com banco mysql.
No volume de 2019 rode o comando.  <br>
<pre>
    mysqldump -u root -p baseDeDados > path/baseDeDados.sql
</pre>
 Esse comando acima vai gerar um arquivo .sql<br>
 no servidor que deseja inserir o backup rode o comando
 <pre>
   mysql -u root -p baseDeDados < path/baseDeDados.sql
 </pre> 
 esse comando acima vai iserir todos os dados do aquivo no banco de dados.<br>
 
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
