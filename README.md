# Calculadora Flutter

Bem-vindo ao projeto **Calculadora Flutter**! Este é um aplicativo de calculadora simples e funcional desenvolvido em Flutter, que implementa operações matemáticas básicas e avançadas, como potenciação e fatorial. O design é minimalista, seguindo especificações detalhadas para proporcionar uma experiência de usuário agradável e intuitiva.

## Sumário

- [Introdução](#introdução)
- [Funcionalidades](#funcionalidades)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Estrutura do Código](#estrutura-do-código)
- [Dependências](#dependências)

## Introdução

Este projeto tem como objetivo criar uma calculadora totalmente funcional em Flutter, seguindo especificações de design detalhadas para garantir uma interface limpa e eficiente. O aplicativo suporta operações matemáticas básicas, como adição, subtração, multiplicação e divisão, bem como operações avançadas, como potenciação e cálculo de fatorial.

## Funcionalidades

- **Operações Básicas**: Adição (`+`), subtração (`-`), multiplicação (`*`), divisão (`/`).
- **Operações Avançadas**:
  - **Potenciação** (`^`): Calcula a potência de um número.
  - **Fatorial** (`!`): Calcula o fatorial de um número inteiro positivo.
- **Entrada de Dados**:
  - Suporta números inteiros e decimais.
  - Botões para `0`, `00` e `.` (ponto decimal).
- **Validação de Expressões**:
  - Impede entradas inválidas, como sequências incorretas de operadores e pontos decimais (por exemplo, `1---2`, `1..234`, `1.234.5`).
- **Limpar Entrada**: Botão `C` para limpar a expressão atual.
- **Resultado**: Botão `=` para calcular e exibir o resultado da expressão.

## Instalação

Para executar este projeto localmente, siga os passos abaixo:

1. **Pré-requisitos**:
   - Flutter SDK instalado. Consulte o [site oficial do Flutter](https://flutter.dev/docs/get-started/install) para instruções de instalação.
   - Editor de código ou IDE compatível com Flutter (por exemplo, Visual Studio Code, Android Studio).

2. **Clonar o Repositório (ou então extraia-o caso tenha acesso ao arquivo .zip)**:
   ```bash
   git clone https://github.com/seu-usuario/calculadora-flutter.git
   ```
   
3. **Navegar para o Diretório do Projeto**:
   ```bash
   cd calculadora-flutter
   ```

4. **Instalar Dependências**:
   ```bash
   flutter pub get
   ```

5. **Executar o Aplicativo**:
   ```bash
   flutter run
   ```
   - Certifique-se de que um dispositivo emulado ou físico esteja conectado e reconhecido pelo Flutter.

## Como Usar

1. **Iniciar o Aplicativo**: Após a instalação, execute o aplicativo em um dispositivo ou emulador compatível.

2. **Inserir Expressões**:
   - Use os botões numéricos para inserir números.
   - Utilize os botões de operação para adicionar operadores matemáticos.
   - O visor exibirá a expressão conforme você insere os valores.

3. **Calcular o Resultado**:
   - Pressione o botão `=` para calcular o resultado da expressão inserida.
   - O resultado será exibido no visor.

4. **Limpar Entrada**:
   - Use o botão `C` para limpar o visor e inserir uma nova expressão.

5. **Considerações**:
   - A calculadora valida as entradas para impedir expressões inválidas.
   - Não é possível iniciar uma expressão com operadores (exceto o sinal de menos `-`).
   - Operadores e pontos decimais duplicados não são permitidos consecutivamente.

## Estrutura do Código

- **main.dart**: Arquivo principal que contém toda a lógica do aplicativo.
  - **CalculadoraApp**: Widget raiz do aplicativo.
  - **CalculadoraHomePage**: StatefulWidget que representa a página principal da calculadora.
  - **CalculadoraHomePageState**: Contém o estado e a lógica da calculadora.
    - **Variáveis**:
      - `inputUser`: String que armazena a expressão inserida pelo usuário.
      - `resultado`: String que armazena o resultado do cálculo.
    - **Métodos**:
      - `build`: Constrói a interface do usuário.
      - `cliqueBotao`: Lida com os eventos de clique nos botões.
      - `calcularResultado`: Processa a expressão e calcula o resultado.
      - `getColorTexto` e `getColorBotao`: Determinam as cores do texto e do fundo dos botões.
      - `isOperador`: Verifica se um caractere é um operador.
      - `fatorial`: Calcula o fatorial de um número inteiro.
  - **BotaoCalculadora**: Widget personalizado para os botões da calculadora.
- **Dependências**:
  - `math_expressions`: Pacote utilizado para avaliar as expressões matemáticas inseridas pelo usuário.

## Dependências

- **Flutter SDK**
- **Pacotes Pub**:
  - [`math_expressions`](https://pub.dev/packages/math_expressions): Utilizado para analisar e avaliar expressões matemáticas.
