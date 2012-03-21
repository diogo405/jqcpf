jqcpf
================

JQuery plugin para validar CPF.

Como funciona?
----------------

O campo de CPF � associado a fun��o do plugin e, quando o campo perde o foco o CPF � validado. Ao final da valida��o o plugin chama a callback de acordo com o resultado.


Uso
----------------
Incluir o JQuery e o plugin na p�gina:

    <script src="http://code.jquery.com/jquery-latest.js"></script>
    <script type="text/javascript" src="jquery.cpf.js"></script>

Criar um campo de texto:

    <input id="campo_cpf" type="text" />

Associar a fun��o ao campo:

	<script>
	$(document).ready(function(){
		$('#campo_cpf').cpf({
			ok: function(cpf) {
				alert('cpf '+cpf+' ok!');
			}
			,nok: function(cpf) {
				alert('cpf '+cpf+' nok :(');
			}
		})
	});
	</script>
	
Quando o CPF � v�lido a callback 'ok' � chamada, caso contr�rio 'nok'.