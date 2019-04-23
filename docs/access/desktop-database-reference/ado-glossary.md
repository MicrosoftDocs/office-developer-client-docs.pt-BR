---
title: Glossário do ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284831"
---
# <a name="ado-glossary"></a>Glossário do ADO

**Aplica-se ao:** Access 2013, Office 2013

## <a name="a"></a>A

**URL absoluta**

Uma URL totalmente qualificada que especifica o local de um recurso que reside na Internet ou em uma intranet. Consulte também **URL** e **URL relativa**.

**Controle ActiveX**

O componente COM de registro automático, em processo, que geralmente tem um elemento visual no tempo de design ou tempo de execução. Os controles ActiveX também têm a capacidade de se comunicar com um contêiner de documento ativo, como o Microsoft Internet Explorer.

**ADISAPI (interface de programação de aplicativo de servidor de dados avançada)**

Uma DLL ISAPI que fornece análise, controle de automação, empacotamento de **Recordset** e empacotamento MIME. O componente ADISAPI funciona por meio da API fornecida pelos serviços de informações da Internet (IIS). ConFira também **ISAPI**.

**função de agregação**

Em uma consulta, uma função como COUNT, AVG ou Desv que calcula um valor usando todas as linhas em uma coluna de uma tabela. Em expressões de gravação e em programação, você pode usar funções agregadas SQL (incluindo as três listadas acima) e funções agregadas de domínio para determinar várias estatísticas.

**alias**

Um nome alternativo que você atribui a uma coluna ou expressão em uma instrução SQL SELECT, geralmente mais curto ou mais significativo. Por exemplo, BobSales é o alias na seguinte instrução SELECT: "Select WR-Sales as BobSales from SalesDB". Um alias pode ser usado para atribuir dinamicamente colunas a associações de controle no objeto **DataControl** .

**segmentação de apartamento**

Um modelo de thread COM onde todas as chamadas a um objeto ocorrem em um thread. No compartimento de apartamento, o COM sincroniza e realiza o marshaling das chamadas. Consulte também **com**.

**operação assíncrona**

Uma operação que retorna o controle para o programa de chamada sem esperar que a operação seja concluída. Antes que a operação seja concluída, a execução do código continua. Consulte também **operação síncrona**.

Retornar ao início

## <a name="b"></a>B

**entrada de vinculação**

Um mapeamento entre um campo em uma tabela e uma variável. Nas extensões do Visual C++ do ADO, os campos do **Recordset** são mapeados para as variáveis C/C++.

**mascara**

Um valor numérico destinado a uma comparação de valor de bit por bit com outros valores numéricos, geralmente para sinalizar as opções no parâmetro ou valores de retorno. Normalmente, essa comparação é feita com operadores lógicos bit a bit, como **e** e **ou** no **&** Visual **|** Basic, e em C++.

Por exemplo, os valores **FieldAttributeEnum** do ADO podem ser usados como bitmasks para determinar os atributos de um campo. Suponha que você quisesse determinar se um campo foi atualizável. Você poderia testar isso com a expressão a seguir no Visual Basic:  
  

Se o resultado for TRUE, o campo será atualizável.

**bookmark**

Um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas para que um usuário possa navegar rapidamente para ela.

**objeto Business**

Um objeto que executa um conjunto definido de operações, como validação de dados ou lógica de regra comercial. Os objetos de negócios geralmente residem na camada intermediária.

**regra de negócios**

A combinação de edições de validação, verificações de logon, pesquisas de banco de dados, políticas e transformações de algoritmos que constituem a maneira de uma empresa de fazer negócios. Também conhecida como *lógica de negócios*.

Retornar ao início

## <a name="c"></a>C

**calculated expression**

Uma expressão que não é constante, mas cujo valor depende de outros valores. Para ser avaliado, uma expressão calculada deve obter e calcular valores de outras fontes, geralmente em outros campos ou linhas.

**módulo**

Uma referência a um intervalo de linhas de uma fonte de dados. No ADO, um capítulo geralmente é uma referência a outro **Recordset**.

As colunas de capítulo permitem definir uma relação *parent-child* em que *parent* representa o **Recordset** contendo a coluna de capítulo, e *child* é o **Recordset** representado pelo capítulo.

**chapter-alias**

Um alias que se refere à coluna acrescentada ao pai.

**conjunto de caracteres**

Um mapeamento de um conjunto de caracteres para seus valores numéricos. Por exemplo, Unicode é um conjunto de caracteres de 16 bits capaz de codificar todos os caracteres conhecidos e usado como um padrão de codificação de caracteres internacional.

**pensão**

O lado dependente de uma relação hierárquica. Um filho é um nó em uma estrutura hierárquica que tem outro nó acima dele (mais próximo da raiz). Consulte também **Child-alias**, **relação pai-filho**, **pai**.

**child-alias**

Um alias que se refere ao filho. Consulte também **alias**, **Child**.

**CLSID (identificador de classe)**

Um identificador universal exclusivo (UUID) que identifica um componente COM. Cada componente COM tem seu CLSID no registro do Windows para que ele possa ser carregado por outros aplicativos. Consulte também **ProgID**, **com**.

**camada de cliente**

Uma camada lógica de um sistema distribuído que geralmente apresenta dados e processa a entrada do usuário, às vezes chamado de *front-end*. Normalmente, a camada de cliente solicita dados de um servidor com base na entrada e, em seguida, formata e exibe o resultado. Consulte também **camada intermediária**, **camada de fonte de dados**, **aplicativo distribuído**.

**COM (modelo de objeto componente)**

Um padrão binário que permite que os objetos interoperem em um ambiente de rede independentemente do idioma em que foram desenvolvidos ou em quais computadores residem. As tecnologias baseadas em COM incluem controles ActiveX, automação e vinculação e incorporação de objetos (OLE). COM permite que um objeto exponha sua funcionalidade a outros componentes e hospede aplicativos. Ele define como o objeto se expõe e como essa exposição funciona nos processos e nas redes. COM também define o ciclo de vida do objeto.

**Componente COM**

Arquivo binário — como. dll,. ocx e alguns arquivos. exe, que dão suporte ao padrão COM para fornecer objetos. Esse arquivo contém código para uma ou mais fábricas de classes, classes COM, mecanismos de entrada de registro, código de carregamento e assim por diante.

**operador de comparação**

Um operador que compara duas expressões e retorna um valor Boolean.

Um parâmetro de critérios que pode ser expresso como\>"" (maior que),\<"" (menor que), "=" (igual),\>"=" (maior que ou igual a)\<, "=" (menor ou igual),\<\>"" (não igual) ou "Like" (correspondência de padrão).

**component**

Um objeto que encapsula tanto dados quanto código e fornece um conjunto bem especificado de serviços publicamente disponíveis.

**arquivo composto**

Uma implementação de armazenamento estruturado COM para arquivos. Um arquivo composto armazena objetos separados em um único arquivo estruturado que consiste em dois elementos principais: objetos de armazenamento e objetos Stream. Juntos, eles funcionam como um sistema de arquivos dentro de um arquivo. Para obter mais informações, consulte arquivos compostos no SDK da plataforma Microsoft.

Um número de arquivos individuais ligados em um arquivo físico. Cada arquivo individual em um arquivo composto pode ser acessado como se fosse um único arquivo físico.

**constante**

Um valor numérico ou de cadeia de caracteres que não é alterado. As enumerações do ADO nomeadas (constantes enumeradas) podem ser usadas em seu código em vez de valores reais, por exemplo, **adUseClient** é uma constante cujo valor é 3. (Const adUseClient = 3). Consulte também **Enumeração**.

**cursor**

Um elemento Database que controla a navegação de registros, a capacidade de atualizidade dos dados e a visibilidade das alterações feitas no banco de dados por outros usuários.

Retornar ao início

## <a name="d"></a>D

**Associação de dados**

O processo de associar os objetos ou os controles de um aplicativo a uma fonte de dados. Um controle associado a uma fonte de dados é chamado de *controle associado a dados*.

O conteúdo de um controle associado a dados é associado a valores de um banco de dados. Por exemplo, um controle de grade que esteja vinculado a um objeto **Recordset** pode ser atualizado quando as linhas no **Recordset** são atualizadas. Quando novos valores são recuperados pelo **Recordset**, novos valores são exibidos na grade.

**provedor de dados**

O software que expõe os dados para um aplicativo ADO diretamente ou por meio de um provedor de serviços. Consulte também **provedor de serviços**.

**Data Shaping**

Uma técnica que usa uma sintaxe formalizada (chamada idioma da **forma**) para definir um objeto **Recordset** especializado (chamado de **Recordset com formato**) que contém não apenas dados, mas também referências a outros objetos **Recordset** e /or valores calculados com base nesses outros objetos **Recordset** .

**camada de fonte de dados**

Uma camada lógica de um sistema distribuído que representa um computador executando um DBMS, como um banco de dados do SQL Server. Consulte também **camada de cliente**, **camada intermediária**, **aplicativo distribuído**.

**PROTOCOLO**

Um protocolo de conexão que permite que componentes COM se comuniquem diretamente entre si através de uma rede. Consulte também **com**, **componente**.

**DDL (linguagem de definição de dados)**

Essas instruções no SQL que definem, em vez de manipular, os dados. O esquema de um banco de dados é criado ou modificado com o DDL. Por exemplo, **CREATE TABLE**, **CREATE INDEX**, **Grant**e **REVOKE** são instruções SQL DDL.

**fluxo padrão**

Um fluxo de texto ou binário (representado por um objeto **Stream** ) associado a objetos **Record** ou **RECORDSET** ao usar determinados provedores OLE DB, como o Microsoft OLE DB Provider for Internet Publishing. O fluxo padrão normalmente contém o conteúdo de um arquivo como o código HTML para a raiz de um site.

**aplicativo distribuído**

Um programa escrito para que o processamento possa ser dividido em vários computadores em uma rede. Normalmente, um aplicativo distribuído é dividido em camadas de apresentação, lógica de negócios e repositório de dados ** ou camadas. Consulte também **camada de cliente**, **camada intermediária**, **camada de fonte de dados**.

**Recordset desconectado**

Um objeto **Recordset** em um cache de cliente que não tem mais uma conexão ativa com o servidor. Se a fonte de dados original precisar ser acessada novamente por algum motivo, como a atualização de dados, a conexão deve ser restabelecida. No enTanto, as coleções, as propriedades e os métodos de um **Recordset** desconectado ainda podem ser acessados.

**DLL (biblioteca de vínculo dinâmico)**

Um arquivo que contém uma ou mais funções que são compiladas, vinculadas e armazenadas separadamente dos processos que as usam. O sistema operacional mapeia as DLLs no espaço de endereço do processo de chamada quando o processo é iniciado ou durante a execução.

**DML (linguagem de manipulação de dados)**

Essas instruções no SQL que manipulam, em oposição a definir, os dados. Os valores em um banco de dados são selecionados e modificados com DML. Por exemplo, **Inserir**, **Atualizar**, **excluir**e **selecionar** são instruções DML SQL.

**provedor de origem do documento**

Uma classe especial de provedores que gerenciam pastas e documentos. Quando um documento é representado por um objeto **Record** , ou uma pasta de documentos é representada por um objeto **Recordset** , o provedor de origem do documento preenche esses objetos com um conjunto exclusivo de campos que descrevem as características do documento, em vez do próprio documento propriamente dito. Consulte também **registro de recurso**.

**DSN (nome da fonte de dados)**

O conjunto de informações usadas para conectar seu aplicativo a um banco de dados ODBC específico. O Gerenciador de driver ODBC usa essas informações para criar uma conexão com o banco de dados. Um DSN pode ser armazenado em um arquivo (um DSN de arquivo) ou no registro do Windows (um DSN de máquina).

**Propriedade Dynamic**

Uma propriedade específica para um provedor de dados ou o serviço de cursor. A coleção **Properties** de um objeto é preenchida com estes automaticamente ("dinamicamente"). Um objeto não tem propriedades dinâmicas até ser conectado a uma fonte de dados por meio de um provedor de dados específico. Consulte também **provedor de dados**, **cursor**.

Retornar ao início

## <a name="e-i"></a>E-I

**Enumeration**

Uma lista de constantes nomeadas. Os valores enumerados não precisam ser exclusivos. No enTanto, o nome de cada valor deve ser exclusivo dentro do escopo onde a enumeração é definida. No ADO, as enumerações são usadas para valores numéricos e de retorno, para adicionar significado ao código do ADO e para proteger o desenvolvedor dos valores numéricos (que podem ser alterados de versão para versão). Por exemplo, para abrir um **conjunto de registros**estático, use o valor enumerado **adOpenStatic** :  
  

Também conhecido como *constante enumerada*. ConFira também **constante**.

**evento**

Uma ação reconhecida por um objeto, para a qual você pode escrever código para responder. Os eventos podem ser gerados pela execução do comando, conclusão de transações, navegação do Recordset e atualizações de dados, entre outras ações. Consulte também **manipulador de eventos**.

**manipulador de eventos**

Um manipulador de eventos é o código que é executado quando ocorre um evento. Consulte também **evento**.

**handler**

Uma rotina que gerencia uma condição ou operação comum e relativamente simples, como recuperação de erro ou gerenciamento de dados.

**Recordset hierárquico**

Um **Recordset** que contém outro **Recordset**. Consulte também **Data Shaping**, **capítulo**.

Para obter mais informações, consulte acEssando [linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md)

**hierarquia**

Em geral, uma hierarquia é uma estrutura classificada com níveis de nível superior e subordinados. No ADO, os **Recordsets** hierárquicos são usados para representar a relação pai-filho entre um registro e um capítulo. Também nos objetos ADO, **Record** e **Stream** podem ser usados para acessar estruturas hierárquicas de árvore, como uma pasta e documentos. O ADO MD também inclui objetos **Hierarchy** para representar uma relação entre os níveis de uma dimensão em um cubo OLAP. ConFira **** também Recordsets hierárquicos, **relação pai-filho**, **capítulo**, **árvore**.

**ISAPI (interface de programação de aplicativo de servidor de Internet)**

Um conjunto de funções para servidores da Internet, como um servidor Windows NT Server/Windows 2000 executando o Microsoft Internet Information Services (IIS).

Retornar ao início

## <a name="k-m"></a>K-M

**key**

Uma coluna ou colunas em uma tabela que identifica exclusivamente uma linha; frequentemente usado para indexar uma tabela.

**empacotamento**

O processo de pacotes, envio e desempacotamento de parâmetros de método de interface nos limites de thread ou de processo.

**camada intermediária**

A camada lógica em um sistema distribuído entre uma interface do usuário ou um cliente da Web e o banco de dados. Normalmente, isso é onde os objetos corporativos são instanciados. A camada intermediária é uma coleção de regras e funções de negócios que geram e operam com informações de recebimento. Eles realizam isso por meio de regras comerciais, que podem ser alteradas com frequência e, portanto, são encapsuladas em componentes que são separados fisicamente da lógica do aplicativo propriamente dita. Também conhecida como *camada de servidor de aplicativos*. Consulte também **aplicativo distribuído**, **camada de cliente**, **camada de fonte de dados**.

**MIME (Multipurpose Internet Mail Extension)**

Um protocolo da Internet originalmente desenvolvido para permitir a troca de mensagens de email com conteúdo avançado em ambientes heterogêneos de rede, computador e email. Na prática, o MIME também foi adotado e estendido por aplicativos que não são de email.

MIME é um padrão que permite que dados binários sejam publicados e lidos na Internet. O cabeçalho de um arquivo com dados binários contém o tipo MIME dos dados; Isso informa aos programas clientes (navegadores da Web e pacotes de email, por exemplo) que eles precisarão manipular os dados de uma maneira diferente de lidar com texto reto. Por exemplo, o cabeçalho de um documento da Web que contém um gráfico JPEG contém o tipo MIME específico para o formato de arquivo JPEG. Isso permite que um navegador exiba o arquivo com seu visualizador JPEG, se houver algum.

Retornar ao início

## <a name="n-o"></a>N-O

**subnó**

Um elemento em uma estrutura de árvore hierárquica. Um nó pode ser a raiz ou o filho de outro nó. Um nó também pode ser pai de vários filhos. Consulte também **hierarquia**, **árvore**, **raiz**, **filho**, **pai**.

**variável de objeto**

Uma variável que contém uma referência para um objeto. Por exemplo, objCustomObject é uma variável que aponta para um objeto do tipo Customobject:  
  
é uma variável que aponta para um objeto do tipo Customobject:  
  
Set objCustomObject = CreateObject (adodb. Conectado

**ODBC**

Uma interface de linguagem de programação padrão usada para se conectar a uma variedade de fontes de dados. Isso é geralmente acessado pelo painel de controle, onde os nomes de fontes de dados (DSNs) podem ser atribuídos para usar drivers ODBC específicos.

**OLE DB**

Um conjunto de interfaces que expõe dados de uma variedade de fontes usando COM. As interfaces OLE DB fornecem aplicativos com acesso uniforme aos dados armazenados em diversas fontes de informação. Essas interfaces dão suporte à quantidade de funcionalidade DBMS apropriada para a fonte de dados, permitindo que ele compartilhe seus dados. Consulte também **com**.

**bloqueio otimista**

Um tipo de bloqueio no qual a página de dados que contém um ou mais registros, incluindo o registro que está sendo editado, não está disponível para outros usuários somente enquanto o registro está sendo atualizado pelo método **Update** , mas está disponível antes e depois da chamada para **Atualizar** .

O bloqueio otimista é usado quando o objeto **Recordset** é aberto com **** o parâmetro LockType ou com a propriedade definida como **adLockOptimistic** ou **adLockBatchOptimistic**. Consulte também **bloqueio pessimista**.

**valor ordinal**

O local numérico de um item em um pedido. Em uma coleção do ADO, o valor ordinal do primeiro item é zero (0). O próximo item é um (1) e assim por diante.

Retornar ao início

## <a name="p"></a>P

**comando com parâmetros**

Uma consulta ou comando que permite que você defina valores de parâmetro antes da execução do comando. Por exemplo, uma cadeia de caracteres SQL pode ser parametrizada por meio da incorporação de marcadores de parâmetro na cadeia de caracteres SQL (designada pelo caractere '? '). O aplicativo especifica valores para cada parâmetro e executa o comando.

**primário**

O lado de controle de uma relação hierárquica. Em uma estrutura hierárquica, um pai tem um ou mais nós filhos diretamente abaixo dele na hierarquia. Consulte também **Parent-alias**, **relação pai-filho**, **filho**.

**parent-alias**

Um alias que se refere ao pai. Consulte também **alias**, **pai**.

**relação pai-filho**

Uma relação em uma estrutura hierárquica na qual o pai é um nível superior e diretamente associado a um ou mais filhos. Um filho é um nível inferior e deve ter um pai. ConFira também **pai**, **filho**.

**persistir**

Para salvar dados em um estado permanente, como salvar um **Recordset** em um arquivo.

**bloqueio pessimista**

Um tipo de bloqueio no qual a página que contém um ou mais registros, incluindo o registro que está sendo editado, não está disponível para outros usuários para garantir que uma atualização seja feita. O comportamento de bloqueio pessimista é definido pelo provedor OLE DB. Normalmente, os registros são bloqueados na edição e permanecem indisponíveis até que o método **Update** seja concluído.

O bloqueio pessimista é habilitado quando o objeto **Recordset** é aberto com o parâmetro **LockType** ou a propriedade definida como **adLockPessimistic**. Consulte também **bloqueio otimista**.

**pool**

Uma otimização de desempenho com base no uso de conjuntos de recursos pré-alocado, como objetos ou conexões de banco de dados. É mais eficiente desenhar um recurso existente do pool do que criar um novo recurso.

**ProgID (identificador programático)**

Um nome exclusivo mapeado para o registro do Windows por um aplicativo COM. O ProgID de uma conexão ADO é "ADODB. Conexão ". Consulte também **CLSID**, **com**.

**proxy**

Um objeto específico de interface que oferece o parâmetro marshaling e a comunicação necessários para um cliente chamar um objeto Application que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo. O proxy está localizado com o cliente e se comunica com um stub correspondente que está localizado com o objeto Application que está sendo chamado. Consulte também **stub**.

Retornar ao início

## <a name="r"></a>R

**URL relativa**

Uma URL parcialmente qualificada que especifica um recurso na Internet ou uma intranet cujo local é relativo a um ponto de partida especificado por uma URL absoluta ou um objeto de conexão ADO equivalente. Em vigor, as URLs absolutas e relativas concatenadas consitute uma URL completa. Consulte também **URL** e **URL absoluta**.

**fonte de dados remota**

Uma fonte de dados que existe em um outro computador, e não no sistema local (onde o aplicativo cliente é executado).

**registro de recurso**

Um registro de um provedor de origem de documento que contém campos para a definição e a descrição de uma pasta ou documento. O documento em si não está contido no registro de recurso, mas geralmente pode ser acessado pelo Stream padrão ou um campo no registro de recurso que contém uma URL. ConFira também o **provedor de origem do documento**, o **fluxo padrão**, a **URL**.

**root**

O nível superior em uma estrutura de árvore hierárquica. O nó raiz não tem pais, mas pode ter filhos. Consulte também **hierarquia**, **árvore**, **pai**, **filho**.

**OPENXML**

Um conjunto de linhas de uma fonte de dados, tudo com o mesmo esquema de campos. Um conjunto de linhas pode representar todos ou alguns campos de uma tabela. Um conjunto de linhas também pode representar uma tabela virtual, criada por uma consulta ou uma junção de duas ou mais tabelas. No ADO, conjuntos de valores são representados por objetos **Recordset** .

Retornar ao início

## <a name="s"></a>S

**esquemas**

Uma descrição de um banco de dados para o sistema de gerenciamento de banco de dados (DBMS), normalmente gerada usando o idioma de definição de dados fornecido pelo DBMS. Um esquema define atributos do banco de dados, como tabelas, colunas e propriedades.

**scope**

O intervalo de referência para um objeto ou uma variável ou um intervalo de registros em um modo de exibição ou tabela. Por exemplo, as variáveis locais podem ser referenciadas somente dentro do procedimento em que foram definidas. As variáveis públicas podem ser acessadas de qualquer lugar no aplicativo. Objetos, como o banco de dados atual, estão no escopo se estiverem no caminho de pesquisa definido. Os intervalos de registros podem ser especificados com uma cláusula Scope em muitos comandos.

**provedor de serviços**

Software que encapsula um serviço, produzindo e consumindo dados, aumentando os recursos em seus aplicativos ADO. É um provedor que não expõe dados diretamente, em vez disso, ele fornece um serviço, como o processamento de consulta. O provedor de serviços pode processar dados fornecidos por um provedor de dados. Consulte também **provedor de dados**.

**Conjunto de registros moldado**

Um **Recordset** cujas colunas foram especificamente definidas para conter não apenas dados, mas também referências (chamados de capítulos) para outros objetos **Recordset** e/ou valores calculados com base em outros objetos **Recordset** .

**An**

Dois ou mais nós em uma estrutura hierárquica que estão no mesmo nível na hierarquia. O nó raiz em uma hierarquia não tem irmãos.

**procedimento armazenado**

Uma coleção pré-compilada de código, como instruções SQL e instruções de controle de fluxo opcionais armazenadas sob um nome e processadas como uma unidade. Procedimentos armazenados são armazenados em um banco de dados; Eles podem ser executados com uma chamada de um aplicativo e permitir variáveis declaradas pelo usuário, execução condicional e outros recursos de programação avançados.

**stub**

Um objeto específico de interface que oferece o parâmetro marshaling e a comunicação necessários para um objeto Application para receber chamadas de um cliente que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo. O stub está localizado com o objeto Application e se comunica com um proxy correspondente localizado com o cliente que o chama. ConFira também **proxy**.

**subnó**

Consulte **Child**.

**operação síncrona**

Uma operação iniciada pelo código que é concluída antes que a próxima operação possa ser iniciada. Consulte também **operação assíncrona**.

Retornar ao início

## <a name="t-w"></a>T-W

**arvore**

Uma estrutura que representa uma relação hierárquica entre os elementos (nós). Há um nó no nível superior de uma árvore (a raiz). Sob a raiz, pode haver vários filhos. Cada filho pode, por sua vez, ser o pai de outros filhos, por isso ramificação como uma árvore. Uma pasta contendo documentos e outras pastas é um exemplo típico de uma estrutura de árvore. Consulte também **hierarquia**, **nó**, **raiz**, **filho**, **pai**.

**URL (Uniform Resource Locator)**

Especifica o local de um recurso que reside na Internet ou em uma intranet. Uma URL completa consiste em um esquema (como FTP, HTTP, mailto, arquivo e assim por diante), seguido por dois-pontos, um nome de servidor e o caminho completo de um recurso (como um documento, gráfico ou outro arquivo). Alguns exemplos de URLs são:  
  
- https://www.domain.com/default.html  
- FTP://ftp.Server.Somewhere/FTP.File  
  
- FTP://ftp.Server.Somewhere/FTP.File  
- file://Server/Share/File.doc

Consulte também **URL absoluta** e **URL relativa**.

**servidor Web**

Um computador que oferece serviços Web e páginas para usuários de intranet e da Internet.



