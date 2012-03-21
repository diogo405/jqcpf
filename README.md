jqcpf
================

JQuery plugin para validar CPF.

Como funciona?
----------------

O campo de CPF é associado a função do plugin e, quando o campo perde o foco o CPF é validado. Ao final da validação o plugin chama a callback de acordo com o resultado.


Uso
----------------
Incluir o JQuery e o plugin na página:

    <script src="http://code.jquery.com/jquery-latest.js"></script>
    <script type="text/javascript" src="jquery.cpf.js"></script>

Criar um campo de texto:

    <input id="campo_cpf" type="text" />

Associar a função ao campo:

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
	
Quando o CPF é válido a callback 'ok' é chamada, caso contrário 'nok'.