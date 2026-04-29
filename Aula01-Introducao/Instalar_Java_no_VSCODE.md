## 1. Verificação de Java ☕

Para verificar se o Java esta instalado. Abra o prompt de comando e digite

```DOS
javac -version
```

Se estiver instalado vai ter um retorno similar à:

```DOS
javac 17.0.2
```

e vai diretamente para o passo 3

Se não estiver instalado vai ter um retorno similar à:

```DOS
"javac" não é reconhecido como um comando interno ou externo
```

e continue na sequencia de passos.

## 2. Instalando Java
### a. Opção 1 no Windows
Se tiver Windows 10 ou superior, pode instalar diretamente no powershell, rodando o seguinte comando:

```PowerShell
winget install Oracle.JDK.21
```
### b. Opção 2 no Windows
Baixe o instalador no site da [Oracle] (https://www.oracle.com/java/technologies/downloads/)

Execute o .msi ou .exe e avance as etapas do instalador.

## 2. Verificação das variáveis de ambiente
Abra o prompt de comando e digite

```DOS
echo %JAVA_HOME%
```

Se a variável de ambiente estiver bem configurada o comando retorna o caminho desta, algo como:

```DOS
C:\Program Files\Java\jdk-21
```

Caso contrario o retorno é o mesmo comando digitado
```DOS
echo %JAVA_HOME%
```
e neste caso deve se proceder a configura a variável de ambiente nas *propiedades do sistema* da seguinte forma:

- Pressione as teclas Windows + R simultaneamente.
- Na caixa que abrir, digite exatamente: sysdm.cpl
- Dê OK.

ao abrir as propiedades do sistema, na aba Avançado:

- Vai em *Variáveis do Sistema*
- Crie uma nova chamada 
- No nome da variável digite *JAVA_HOME*
- No valor da variável digite o caminho da pasta onde o Java foi instalado (ex: C:\Program Files\Eclipse Foundation\jdk-21.0.x).
- Dê OK.

Edite a variável Path e adicione o item %JAVA_HOME%\bin.
- Vai em *Variáveis de usuário para...*
- Procure *Path* e clique em editar
- Clique em *Novo*
- Adicione *%JAVA_HOME%\bin*
- 
- 

