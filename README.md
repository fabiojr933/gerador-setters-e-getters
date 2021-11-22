# PHPSetter

É uma simples ferramenta que pode ser executada em qualquer navegador web. 

Com ela o desenvolvedor PHP pode facilmente inserir o nome de suas variáveis que a aplicação vai gerar uma classe completa com os métodos Getter, Setter e Constructor.

A utilização dessa ferramenta é muito simples, ela é composta por algumas etapas e regras para que tudo funcione corretamente.


Confira nosso exemplo em funcionamento



# Declaring the variables/Declarando as variáveis

No campo Variables, você precisa inserir o nome das variáveis, sem $ e também sem delcarar a visibilidade

> **Right/Certo**
```
name
email
password
```

> **Wrong/Errado**
```
private $name;
$email
password;
name email password
```


# Getter, Setter And Construtor
Existem três checkbox, que por padrão estão ativos, você pode optar em não seleciona-los antes de gerar o código. 

## Setter
Quando essa opção estiver marcada, cria os métodos Setter, como mostra o bloco abaixo.

```php
public function setName($Name){
  $this->name = $Name;
}
```

## Getter
Quando essa opção estiver marcada, será criado os métodos Getters, como mostra o código abaixo.

```php
public function getName(){
  return $this->name;
}
```

## Constructor
O construtor é um método opcional para muitos desenvolvedores, porém quando ele estiver marcado, será criado os atributos com todos os parâmetros pré-definidos no método. Veja um exeplo abaixo.

```php
public function __construct($name, $email, $password){
  $this->name = $name;
  $this->email = $email;
  $this->password = $password;
}
```

# Final Result/Resultado Final
```php
<?php
	namespace ../../;

	class ClassName{

		private $name;
		private $email;

		public function __construct($name, $email){
			$this->name = $name;
			$this->email = $email;
		}
		public function setName($Name){
			$this->name = $Name;
		}

		public function setEmail($Email){
			$this->email = $Email;
		}

		public function getName(){
			 return $this->name;
		}

		public function getEmail(){
			 return $this->email;
		}

	}
?>
```
