# Tópico e Material ainda em Costrução

<p align="center">
  <img src="https://img.shields.io/badge/versão-1.0-blue" alt="Versão">
  <img src="https://img.shields.io/badge/status-em%20desenvolvimento-yellow" alt="Status do Curso">
  <img src="https://img.shields.io/badge/feito%20com-Python%203.x-blue?logo=python&logoColor=white" alt="Feito com Python">
  <img src="https://img.shields.io/badge/licença-MIT-green" alt="Licença">
</p>

<p align="center">
  <img src="assets/banner_python101.png" width="400" alt="Python101 Logo">
</p>

# 🐍 python101
## Professor, Dr. Vinícius Costa Amador 
### ✨ Seja bem-vindo(a)! Este material foi preparado com carinho para acolher você no curso de Python do ciclo básico de programação. Espero que aproveite bastante e que o conteúdo te ajude a crescer! ✨ Welcome! This material was lovingly prepared to welcome you to the Python course for the basic programming cycle. I hope you enjoy it and that it helps you grow! ✨ 欢迎！本课程材料是我用心准备的，旨在欢迎你加入 Python 编程基础课程。希望你能从中受益，不断成长！

---

# Sumário – Programação Orientada a Objetos (POO)
- Fundamentos da POO
  -  1.1 O que é Programação Orientada a Objetos
  -  1.2 Diferença entre POO e Programação Estruturada
  -  1.3 Vantagens da Programação Orientada a Objetos
- Elementos Básicos
  -  2.1 Classe
  -  2.2 Objeto
- Princípios Fundamentais
  -  3.1 Encapsulamento
  -  3.2 Herança
  -  3.3 Polimorfismo
  -  3.4 Abstração
- Relações Entre Classes
  -  4.1 Associação
  -  4.2 Agregação
  -  4.3 Composição
  -  4.4 Generalização e Especialização
- Elementos Avançados
  -  5.1 Interfaces
  -  5.2 Sobrecarga de Métodos (Overloading)
  -  5.3 Sobrescrita de Métodos (Overriding)
- Boas Práticas e Design
  -  6.1 Princípios SOLID
  -  6.2 Padrões de Projeto (Design Patterns)
  -  6.3 Modelagem com UML

---

## 1. Fundamentos da POO
### 1.1 O que é Programação Orientada a Objetos
A Programação Orientada a Objetos (POO) é um paradigma de programação baseado no conceito de "objetos", que podem conter dados (atributos) e código (métodos). Ao invés de focar apenas em funções e lógica, como na programação estruturada, a POO organiza o código em unidades reutilizáveis e representações do mundo real.

Esse paradigma permite representar conceitos como "Pessoa", "Carro", ou "ContaBancária" como objetos em um programa, facilitando o entendimento, manutenção e expansão do código.

#### Exemplos didáticos clássicos:
Pessoa: um objeto do tipo "Pessoa" pode ter atributos como nome, idade e CPF, e métodos como falar() ou andar().
Carro: um objeto do tipo "Carro" pode ter atributos como cor, modelo e velocidade, e métodos como acelerar() e frear().
- Conta Bancária: com atributos como saldo e titular, e métodos como sacar() e depositar().

Esses exemplos mostram como a POO ajuda a estruturar o código de forma mais natural, próxima do pensamento humano e da lógica do mundo real.

### 1.2 Diferença entre POO e Programação Estruturada
A principal diferença entre a Programação Orientada a Objetos (POO) e a Programação Estruturada está na forma como o código é organizado e no foco da modelagem.

| Aspecto                     | Programação Estruturada                           | Programação Orientada a Objetos                     |
|----------------------------|---------------------------------------------------|----------------------------------------------------|
| **Organização**            | Baseada em funções e procedimentos                | Baseada em objetos (instâncias de classes)         |
| **Foco**                   | Ações e lógica sequencial                         | Entidades que encapsulam dados e comportamentos    |
| **Reutilização de código** | Baixa, depende de copiar e adaptar funções        | Alta, com herança, polimorfismo e composição       |
| **Manutenção**             | Mais difícil em sistemas grandes                  | Facilitada por modularização e encapsulamento      |
| **Extensibilidade**        | Limitada                                          | Facilitada por abstração e herança                 |
| **Exemplo mental**         | Receita de bolo passo a passo                     | Modelo de um bolo com propriedades e métodos       |


A Programação Estruturada se baseia em funções e procedimentos, sendo linear e sequencial. Já a POO organiza o código em objetos, que encapsulam dados e comportamentos relacionados.

#### Exemplo didático:
#### Suponha um sistema bancário:
Na Programação Estruturada, você teria várias funções como sacar(conta, valor) e depositar(conta, valor).
Na POO, você teria uma classe ContaBancaria com métodos sacar() e depositar() definidos dentro da própria classe, junto com os dados (como saldo e titular).
Isso torna a POO mais próxima da maneira como pensamos sobre objetos e comportamentos no mundo real.

### 1.3 Vantagens da POO
A Programação Orientada a Objetos traz uma série de benefícios que facilitam o desenvolvimento de sistemas complexos, tornando o código mais modular, reutilizável e fácil de manter.

#### Principais vantagens:
- Modularidade: o sistema é dividido em partes independentes (classes), o que permite isolar problemas e facilitar testes.
- Reutilização: com a herança, é possível reaproveitar código de classes existentes.
Facilidade de manutenção: alterações em uma parte do código tendem a não afetar outras partes, desde que bem encapsuladas.
- Extensibilidade: é fácil estender funcionalidades criando novas classes que herdarem comportamentos existentes.
- Mapeamento com o mundo real: objetos representam entidades reais, facilitando a modelagem e o entendimento do sistema.

#### Exemplo didático:
Imagine um sistema escolar com uma classe "Pessoa" e subclasses "Aluno" e "Professor". A classe "Pessoa" tem atributos como nome e CPF. "Aluno" pode herdar esses atributos e adicionar matrícula, enquanto "Professor" pode adicionar salário e disciplina. Assim, o código fica mais limpo e reutilizável, evitando duplicações e facilitando modificações futuras.

## 2. Elementos Básicos
### 2.1 Classe
Uma classe é uma estrutura que serve como um molde para criar objetos. Ela define os atributos (dados) e os métodos (comportamentos) que seus objetos terão. Pense na classe como a planta de uma casa: ela não é a casa em si, mas descreve como a casa deve ser construída.

#### Atributos e métodos
- Atributos: variáveis que armazenam o estado do objeto.
- Métodos: funções definidas dentro da classe que descrevem os comportamentos do objeto.

#### Visibilidade
- Pública (public): acessível de qualquer lugar.
- Privada (private): acessível apenas de dentro da própria classe (em Python, usa-se a convenção _nome ou __nome).
- Protegida (protected): acessível apenas na própria classe e em subclasses (em Python, por convenção, _nome).

#### Construtores e destrutores
- Construtor (__init__): método especial chamado automaticamente ao instanciar a classe.
- Destrutor (__del__): método chamado quando o objeto é destruído (pouco utilizado em Python).

#### Exemplo em Python:
```python
class Pessoa:
    def __init__(self, nome, idade):  # Construtor
        self.nome = nome              # Atributo
        self.idade = idade

    def apresentar(self):             # Método
        print(f"Olá, meu nome é {self.nome} e tenho {self.idade} anos.")

    def envelhecer(self):             # Outro método
        self.idade += 1
```

Neste exemplo, a classe Pessoa tem dois atributos (nome e idade) e dois métodos (apresentar e envelhecer). O método __init__ é o construtor e é executado sempre que criamos uma nova Pessoa.

#### Exemplo de uso:
```python
p1 = Pessoa("João", 30)
p1.apresentar()       # Saída: Olá, meu nome é João e tenho 30 anos.
p1.envelhecer()
p1.apresentar()       # Saída: Olá, meu nome é João e tenho 31 anos.
```

A classe é a base da programação orientada a objetos. É por meio dela que organizamos e estruturamos nosso código de forma clara e reutilizável.

### 2.2 Objeto
Um objeto é uma instância de uma classe. Ele representa uma entidade concreta do mundo real dentro do programa, com características próprias (atributos) e comportamentos definidos (métodos). Cada objeto criado a partir de uma mesma classe pode ter valores diferentes para seus atributos.

- Instanciação de objetos: Instanciar um objeto significa criar um novo elemento baseado em uma classe, utilizando o construtor dessa classe.
- Estado e comportamento:
  -  Estado: é representado pelos valores atuais dos atributos do objeto.
  -  Comportamento: é determinado pelos métodos que o objeto pode executar.
- Acesso a atributos e métodos:
Em Python, os atributos e métodos são acessados usando a notação de ponto (objeto.atributo ou objeto.metodo()).

#### Exemplo:
Usando a classe Pessoa definida anteriormente:
```python
p1 = Pessoa("João", 30)  # instância de Pessoa
p2 = Pessoa("Maria", 25)  # outra instância

p1.apresentar()  # Saída: Olá, meu nome é João e tenho 30 anos.
p2.apresentar()  # Saída: Olá, meu nome é Maria e tenho 25 anos.
```

Neste exemplo, p1 e p2 são dois objetos diferentes criados a partir da classe Pessoa. Cada um possui seu próprio estado (nome e idade), mas compartilham o mesmo comportamento (métodos definidos na classe).

Objetos são as unidades fundamentais da POO. Eles permitem encapsular dados e comportamentos, facilitando a organização e a modularização dos sistemas.

## 3. Princípios Fundamentais
### 3.1 Encapsulamento
O encapsulamento é o princípio da POO que consiste em esconder os detalhes internos de implementação de uma classe, expondo apenas o que é necessário por meio de métodos públicos. Isso protege os dados e facilita a manutenção do código.

Ao encapsular os atributos, evita-se que partes externas do programa acessem ou modifiquem diretamente os dados da classe, garantindo maior segurança e controle.

- Métodos de acesso (getters e setters)
  -  Getter: método para acessar um atributo privado.
  -  Setter: método para modificar um atributo privado.

#### em Python:
```python
class ContaBancaria:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.__saldo = saldo  # atributo privado

    def get_saldo(self):
        return self.__saldo

    def set_saldo(self, novo_saldo):
        if novo_saldo >= 0:
            self.__saldo = novo_saldo
        else:
            print("Saldo inválido!")
```

Exemplo de uso:

```python
conta = ContaBancaria("Ana", 1000)
print(conta.get_saldo())    # Saída: 1000
conta.set_saldo(1500)
print(conta.get_saldo())    # Saída: 1500
conta.set_saldo(-500)       # Saída: Saldo inválido!
```

Esse princípio melhora a confiabilidade e a robustez dos sistemas, permitindo mudanças internas sem afetar o restante do código.
  -  Ocultação de dados
  -  Métodos de acesso (getters e setters)

### 3.2 Herança
A herança permite que uma classe (chamada de classe derivada ou subclasse) herde atributos e métodos de outra classe (chamada de classe base ou superclasse). Isso promove a reutilização de código e facilita a criação de hierarquias.
- Hierarquia de classes
  -  Uma classe derivada pode estender ou especializar o comportamento da classe base.
  -  Em Python, a herança é definida ao passar a classe base entre parênteses na definição da nova classe.
- Herança simples e múltipla
  -  Simples: herda de uma única classe.
  -  Múltipla: herda de duas ou mais classes (suportada em Python, mas deve ser usada com cuidado).

#### Exemplo em Python:
```python
# INÍCIO DO SCRIPT
class Animal:
    def falar(self):
        print("Som")
class Cachorro(Animal):
    def falar(self):
        print("Latido")
# FIM DO SCRIPT
```

Exemplo de uso
```python
aluno = Aluno("Carlos")
aluno.falar()     # Saída: Carlos está falando.
aluno.estudar()   # Saída: Carlos está estudando.
```

A herança permite criar sistemas mais flexíveis, evitando duplicação de código e facilitando a organização das responsabilidades.
  -  Reutilização de código
  -  Hierarquia de classes
  -  Herança simples e múltipla

### 3.3 Polimorfismo
O polimorfismo permite que objetos de diferentes classes possam ser tratados de forma uniforme, compartilhando a mesma interface ou método, mas com comportamentos distintos. Isso proporciona flexibilidade e extensibilidade ao código.

Tipos de Polimorfismo

 - Polimorfismo em tempo de compilação (sobrecarga): mesma função com diferentes assinaturas (número ou tipo de parâmetros). Em Python, não é suportado diretamente, mas pode ser simulado.
 - Polimorfismo em tempo de execução (sobrescrita): uma subclasse reimplementa um método da superclasse.

#### Exemplo:
```python
class Animal:
    def emitir_som(self):
        print("Som genérico de animal")

class Cachorro(Animal):
    def emitir_som(self):
        print("Latido")

class Gato(Animal):
    def emitir_som(self):
        print("Miau")
```
#### Exemplo:
```python
animais = [Cachorro(), Gato(), Animal()]
for animal in animais:
    animal.emitir_som()
# Saída:
# Latido
# Miau
# Som genérico de animal
```

O método emitir_som() é chamado de forma polimórfica, e o comportamento depende da classe real do objeto.

 - Polimorfismo em tempo de compilação (sobrecarga)
 - Polimorfismo em tempo de execução (sobrescrita)

### 3.4 Abstração
A abstração consiste em representar entidades do mundo real com um nível adequado de detalhe, ocultando a complexidade desnecessária. Em POO, usamos a abstração para focar no que um objeto faz, e não em como ele faz.

#### Classes e métodos abstratos

 - Uma classe abstrata serve como base para outras classes e não pode ser instanciada diretamente.
 - Um método abstrato é um método declarado mas não implementado; as subclasses devem implementar sua lógica.

Em Python, usamos o módulo abc para criar classes abstratas.

#### Exemplo em Python:

```python
from abc import ABC, abstractmethod

class FormaGeometrica(ABC):
    @abstractmethod
    def calcular_area(self):
        pass

class Quadrado(FormaGeometrica):
    def __init__(self, lado):
        self.lado = lado

    def calcular_area(self):
        return self.lado ** 2
```

#### Exemplo de uso:

```python
q = Quadrado(4)
print(q.calcular_area())  # Saída: 16
```

A abstração ajuda a criar códigos mais organizados e reutilizáveis, forçando uma estrutura clara e consistente para as subclasses.

 - Representação simplificada de conceitos
 - Classes e métodos abstratos

## 4. Relações Entre Classes
4.1 AssociaçãoA associação representa um relacionamento entre dois objetos, onde um conhece o outro e pode usar seus atributos ou métodos. Essa relação não indica posse ou dependência, apenas que existe um vínculo entre os objetos.

#### Exemplo em Python:
```python
class Professor:
    def __init__(self, nome):
        self.nome = nome

class Disciplina:
    def __init__(self, nome, professor):
        self.nome = nome
        self.professor = professor

prof = Professor("João")
disc = Disciplina("Matemática", prof)
print(disc.professor.nome)  # Saída: João
```

### 4.2 Agregação
A agregação é um tipo especial de associação onde uma classe contém outra, mas os objetos agregados podem existir de forma independente. Representa uma relação do tipo "tem um".

#### Exemplo em Python:
```python
class Departamento:
    def __init__(self, nome):
        self.nome = nome

class Universidade:
    def __init__(self):
        self.departamentos = []

    def adicionar_departamento(self, departamento):
        self.departamentos.append(departamento)

dep = Departamento("Engenharia")
univ = Universidade()
univ.adicionar_departamento(dep)
print(univ.departamentos[0].nome)  # Saída: Engenharia
```

#### 4.3 Composição

A composição é uma relação mais forte que a agregação. Se o objeto composto for destruído, os objetos componentes também o serão. Indica dependência total.

#### Exemplo em Python:
```python
class Motor:
    def __init__(self):
        self.potencia = "100cv"

class Carro:
    def __init__(self):
        self.motor = Motor()  # Composição

c = Carro()
print(c.motor.potencia)  # Saída: 100cv
```

#### 4.4 Generalização e Especialização
A generalização ocorre quando classes compartilham características comuns que são extraídas para uma superclasse. A especialização é o processo inverso, no qual subclasses refinam ou estendem o comportamento da superclasse.

#### Exemplo em Python:
```python
class Funcionario:
    def __init__(self, nome):
        self.nome = nome

class Gerente(Funcionario):
    def __init__(self, nome, setor):
        super().__init__(nome)
        self.setor = setor

g = Gerente("Ana", "TI")
print(g.nome, g.setor)  # Saída: Ana TI
```
Essas relações ajudam a estruturar melhor os sistemas orientados a objetos, refletindo a complexidade e interdependência entre os elementos do mundo real.

### 5. Elementos Avançados

#### 5.1 Interfaces
Uma interface define um contrato que uma classe deve cumprir. Ela especifica os métodos que devem ser implementados, mas não fornece sua implementação. Em Python, interfaces são geralmente representadas por classes abstratas com apenas métodos abstratos.

Diferença entre interface e classe abstrata

 - Interface: todos os métodos são abstratos, sem implementação.
 - Classe abstrata: pode conter tanto métodos abstratos quanto métodos com implementação.

Exemplo em Python:

```python
from abc import ABC, abstractmethod

class IImprimivel(ABC):
    @abstractmethod
    def imprimir(self):
        pass

class Documento(IImprimivel):
    def __init__(self, titulo):
        self.titulo = titulo

    def imprimir(self):
        print(f"Imprimindo documento: {self.titulo}")
```

Exemplo de uso:

```python
doc = Documento("Contrato")
doc.imprimir()  # Saída: Imprimindo documento: Contrato
```

O uso de interfaces promove a padronização e a flexibilidade, permitindo que diferentes classes implementem comportamentos comuns de forma independente.

### 5.2 Sobrecarga de Métodos (Overloading)
A sobrecarga de métodos ocorre quando métodos com o mesmo nome são definidos com diferentes conjuntos de parâmetros. Em Python, a sobrecarga tradicional não é suportada de forma nativa, mas pode ser simulada com argumentos padrão ou uso de *args e **kwargs.

#### Exemplo em Python (simulado):

```python
class Calculadora:
    def somar(self, a, b=0, c=0):
        return a + b + c
```

Exemplo de uso:

```python
calc = Calculadora()
print(calc.somar(2, 3))       # Saída: 5
print(calc.somar(1, 2, 3))    # Saída: 6
```

Essa técnica proporciona maior flexibilidade no uso dos métodos, mesmo em uma linguagem que não suporta sobrecarga direta.

### 5.3 Sobrescrita de Métodos (Overriding)
A sobrescrita de métodos ocorre quando uma subclasse redefine um método da sua superclasse, modificando seu comportamento. Essa é uma aplicação prática do polimorfismo.

#### Exemplo em Python:

```python
class Animal:
    def falar(self):
        print("Animal fazendo som")

class Cachorro(Animal):
    def falar(self):
        print("O cachorro late")
```

Exemplo de uso:

```python
a1 = Animal()
a2 = Cachorro()
a1.falar()  # Saída: Animal fazendo som
a2.falar()  # Saída: O cachorro late
```

A sobrescrita permite adaptar comportamentos herdados às necessidades específicas das subclasses.

## 6. Boas Práticas e Design

### 6.1 Princípios SOLIDOs princípios SOLID são boas práticas para desenvolver sistemas orientados a objetos mais organizados, reutilizáveis e de fácil manutenção.

- Responsabilidade Única: cada classe deve ter apenas uma responsabilidade. Exemplo: separar a lógica de cadastro da lógica de envio de e-mails.
- Aberto/Fechado: o código deve estar aberto para extensão, mas fechado para modificação. Exemplo: usar herança para adicionar funcionalidades sem alterar a classe base.
- Substituição de Liskov: subclasses devem poder ser usadas no lugar de suas superclasses. Exemplo: um Gerente deve funcionar como um Funcionario sem erros.
- Segregação de Interface: interfaces específicas são melhores que interfaces genéricas. Exemplo: separar interfaces IImprimivel e IEscaneavel em vez de uma só com muitos métodos.
- Inversão de Dependência: classes devem depender de abstrações, e não de implementações concretas. Exemplo: injetar uma interface como dependência ao invés de uma classe fixa.

### 6.2 Padrões de Projeto (Design Patterns)Padrões de projeto são soluções reutilizáveis para problemas comuns em projetos orientados a objetos.

- Singleton: garante que uma classe tenha uma única instância.

```python
class Singleton:
    _instancia = None
    def __new__(cls):
        if cls._instancia is None:
            cls._instancia = super(Singleton, cls).__new__(cls)
        return cls._instancia
```

- Factory: cria objetos sem expor a lógica de criação.

```python
class Animal:
    def falar(self):
        pass

class Cachorro(Animal):
    def falar(self):
        print("Au au")

class FabricaAnimal:
    def criar(self, tipo):
        if tipo == "cachorro": return Cachorro()
```

- Observer: objetos observam outro objeto e são notificados quando ele muda.
- Strategy: encapsula algoritmos intercambiáveis. Útil para aplicar diferentes comportamentos em tempo de execução.
- Decorator: adiciona funcionalidades a um objeto dinamicamente, sem alterar sua estrutura.

6.3 Modelagem com UMLA UML é uma linguagem visual para modelar sistemas orientados a objetos.

- Diagrama de classes: mostra classes, atributos, métodos e relações entre classes.
- Diagrama de sequência: mostra a interação temporal entre objetos.
- Diagrama de objetos: mostra instâncias de classes em um determinado momento do tempo.

