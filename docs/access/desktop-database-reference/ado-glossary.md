---
title: Glossário do ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9b9fd656aeda727cc829ab47ea4cb9fab8f2a169
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997788"
---
# <a name="ado-glossary"></a>Glossário do ADO

**Aplica-se a**: Access 2013, o Office 2013

## <a name="a"></a>A

**URL absoluta**

Uma URL totalmente qualificada que especifica o local de um recurso que reside na Internet ou intranet. Consulte também **URL** e a **URL relativa**.

**Controle ActiveX**

Registro automático no processo componente COM que geralmente tem um elemento visual no tempo de design ou tempo de execução. Controles ActiveX também têm a capacidade de se comunicar com um contêiner do documento ativo, como o Microsoft Internet Explorer.

**ADISAPI (avançado a Interface de programação de aplicativo do servidor de Internet dados)**

Uma DLL ISAPI que fornece a análise, controle de automação, **Recordset** empacotamento e empacotamento de MIME. O componente ADISAPI funciona por meio da API fornecida pelo serviços de informações da Internet (IIS). Consulte também **ISAPI**.

**função de agregação**

Em uma consulta, uma função como COUNT, AVG ou STDEV que calcula um valor usando todas as linhas em uma coluna de uma tabela. Em expressões de gravação e em programação, você pode usar funções agregadas do SQL (incluindo os três listados acima) e funções agregadas de domínio para determinar diversas estatísticas.

**alias**

Um nome alternativo dado a uma coluna ou expressão em uma instrução SQL SELECT, geralmente menor ou mais significativa. Por exemplo, BobSales é o alias na instrução SELECT a seguir: "Selecione wr-vendas como BobSales do SalesDB". Um alias pode ser usado para atribuir dinamicamente colunas para controlar as ligações no objeto **DataControl** .

**apartment threading**

Uma COM onde todas as chamadas para um objeto ocorrerem em um segmento de modelo de threading. Em apartment threading, COM sincroniza e controla chamadas. Consulte também **COM**.

**operação assíncrona**

Uma operação que devolve o controle para o programa de chamada sem esperar que a operação seja concluída. Antes que a operação for concluída, continua a execução do código. Consulte também **operação síncrona**.

Retornar ao início

## <a name="b"></a>B

**entrada de ligação**

Um mapeamento entre um campo em uma tabela e uma variável. As extensões do Visual C++ do ADO, os campos de **Recordset** são mapeados para variáveis C/C++.

**máscara de bits**

Um valor numérico destinado para obter uma comparação de valor de bit a bit com outros valores numéricos, geralmente sinalizar opções no parâmetro ou valores de retorno. Geralmente, essa comparação é feita com operadores lógicos, como **e** e **ou** no Visual Basic, **&** e **|** no C++.

Por exemplo, os valores de ADO **FieldAttributeEnum** podem ser usados como bitmasks para determinar os atributos de um campo. Suponha que você queria saber se um campo teve atualizável. Você pode testar isso com a expressão a seguir no Visual Basic:  
  

Se o resultado for TRUE, o campo é atualizável.

**bookmark**

Um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas, para que um usuário pode navegar rapidamente para ele.

**objeto de negócios**

Um objeto que executa um conjunto definido de operações, como a lógica de regra comercial ou de validação de dados. Objetos comerciais geralmente residem na camada intermediária.

**regra de negócio**

A combinação das edições de validação, verificações de logon, pesquisas de banco de dados, políticas e algoritmos transformações que constituem a maneira de uma empresa de fazer negócios. Também conhecida como *a lógica de negócios*.

Retornar ao início

## <a name="c"></a>C

**expressão calculada**

Uma expressão que não é uma constante, mas cujo valor depende de outros valores. Para ser avaliada, uma expressão calculada deve obter e computar valores de outras fontes, geralmente em outros campos ou linhas.

**chapter**

Uma referência a um intervalo de linhas de uma fonte de dados. No ADO, um capítulo normalmente é uma referência para outro **conjunto de registros**.

Colunas de capítulo tornam possível definir uma relação *pai-filho* onde o *pai* é o **Recordset** que contém a coluna de capítulo e o *filho* é o **conjunto de registros** representados pelo capítulo.

**chapter-alias**

Um alias que se refere à coluna acrescentada ao pai.

**conjunto de caracteres**

Um mapeamento de um conjunto de caracteres para seus valores numéricos. Por exemplo, Unicode é um caractere de 16 bits definida capaz de codificação de todos os caracteres conhecidos e usadas como um padrão mundial de codificação de caracteres.

**filho**

O lado dependente de uma relação hierárquica. Um filho é um nó em uma estrutura hierárquica que tem outro nó acima dele (próximo da raiz). Consulte também **filho-alias**, **relação pai-filho**, **pai**.

**child-alias**

Um alias que se refere ao filho. Consulte também **alias**, **filho**.

**CLSID (identificador de classe)**

Um identificador universal exclusivo (UUID) que identifica um componente COM. Cada componente COM tem sua CLSID no registro do Windows para que possa ser carregado por outros aplicativos. Consulte também **ProgID**, **COM**.

**camada do cliente**

Uma camada lógica de um sistema distribuído que geralmente apresenta dados e processa a entrada do usuário, às vezes chamado de *front-end*. Geralmente, a camada de cliente solicita dados de um servidor com base na entrada e formata e exibe o resultado. Consulte também **camada intermediária**, **camada de fonte de dados**, **aplicativos distribuídos**.

**COM (modelo de objeto componente)**

Binário padrão que permite a objetos interoperar em um ambiente de rede independentemente do idioma no qual eles foram desenvolvidos ou em quais computadores eles residem. Baseado em COM tecnologias incluem os controles ActiveX, automação e objeto vinculação e incorporação de objetos (OLE). COM permite que um objeto expor sua funcionalidade a outros componentes e para hospedar aplicativos. Ele define como o objeto expõe próprio tanto como essa exposição funciona nos processos e nas redes. COM também define o ciclo de vida do objeto.

**Componente COM**

Arquivo binário — como. dll,. ocx e alguns arquivos .exe — que suporta padrão COM o fornecimento de objetos. Esse arquivo contém o código para um ou mais criações de classes, classes COM, mecanismos de entrada de registro, códigos de carregamento e assim por diante.

**operador de comparação**

Um operador que compara duas expressões e retorna um valor Boolean.

Um parâmetro de critérios que pode ser expresso como "\>"(maior que),"\<"(menor que), "=" (igual a),"\>=" (maior que ou igual), "\<=" (menor ou igual), "\<\>" (não igual a), ou "como" (padrão correspondente).

**componente**

Um objeto que encapsula dados e código e fornece um conjunto de serviços disponíveis publicamente bem especificado.

**arquivo composto**

Uma implementação do COM o armazenamento para arquivos de estruturado. Um arquivo composto armazena objetos separados em um único arquivo estruturado consiste em dois elementos principais: objetos stream e objetos de armazenamento. Juntos, eles funcionam como um sistema de arquivos dentro de um arquivo. Para obter mais informações, consulte arquivos compostos no Microsoft Platform SDK.

Um número de arquivos individuais acoplado juntos em um arquivo físico. Cada arquivo individual em um arquivo composto pode ser acessado como se fosse um único arquivo físico.

**constante**

Um valor numérico ou cadeia de caracteres que não é alterado. Enumerações do ADO nomeadas (constantes enumeradas) podem ser usadas em seu código, em vez de valores reais, por exemplo, **adUseClient** é uma constante cujo valor é 3. (AdUseClient const = 3). Consulte também **enumeração**.

**cursor**

Um elemento de banco de dados que controla a navegação de registro, atualização de dados e a visibilidade das alterações feitas no banco de dados por outros usuários.

Retornar ao início

## <a name="d"></a>D

**vinculação de dados**

O processo de associar os objetos ou controles de um aplicativo para uma fonte de dados. Um controle associado a uma fonte de dados é chamado de um *controle acoplado a dados*.

O conteúdo de um controle acoplado a dados está associado com valores de um banco de dados. Por exemplo, um controle de grade que está acoplado a um objeto **Recordset** pode ser atualizado quando as linhas no **conjunto de registros** são atualizadas. Quando novos valores são recuperados pelo **Recordset**, novos valores são exibidos na grade.

**provedor de dados**

Software que expõe os dados para um aplicativo ADO diretamente ou por meio de um provedor de serviços. Consulte também o **provedor de serviços**.

**Data shaping**

Uma técnica que faz uso de sintaxe formal (chamada de **idioma da forma**), para definir um objeto **Recordset** especializado (chamado de um **Recordset com formato**) que contém não apenas os dados, mas também faz referência a outros objetos **Recordset** e / ou computado valores com base nesses outros objetos **Recordset** .

**camada de fonte de dados**

Uma camada lógica de um sistema distribuído que representa um computador que executa um DBMS, como um banco de dados do SQL Server. Consulte também **camada do cliente**, **aplicativo distribuído**e **camada intermediária**.

**DCOM**

Um protocolo de transmissão que permite que os componentes se comunicarem diretamente entre si através de uma rede. Consulte também **COM**, **componente**.

**DDL (linguagem de definição de dados)**

Essas instruções no SQL que definem, em oposição a manipulação de dados. O esquema de banco de dados é criado ou modificado com DDL. Por exemplo, **CREATE TABLE**, **CREATE INDEX**, **CONCEDER**e **REVOGAR** são instruções SQL DDL.

**fluxo padrão**

Um texto ou o fluxo binário (representado por um objeto **Stream** ) que está associado a objetos **Record** ou um **Recordset** ao usar alguns provedores do OLE DB, como o Microsoft OLE DB Provider for Internet Publishing. Normalmente, um fluxo padrão contém o conteúdo de um arquivo, como o código HTML para a raiz de um site.

**aplicativos distribuídos**

Um programa escrito para que o processamento pode ser dividido em vários computadores em uma rede. Normalmente, um aplicativo distribuído é dividido em *camadas*e camadas de repositório de dados, lógica de negócios ou apresentação. Consulte também **camada do cliente**, a **camada intermediária**, a **camada de fonte de dados**.

**conjunto de registros desconectado**

Um objeto **Recordset** em um cache de cliente que não tem mais uma conexão ao vivo para o servidor. Se a fonte de dados original precisar ser acessado novamente por algum motivo, como atualização de dados, a conexão deve ser restabelecida. No entanto, as coleções, propriedades e métodos de um **Recordset** de desconectados podem ainda ser acessados.

**DLL (biblioteca de vínculo dinâmico)**

Um arquivo que contém uma ou mais funções que são compiladas, vinculadas e armazenados separadamente dos processos que usá-los. O sistema operacional mapeia as DLLs no espaço de endereço do processo chamado quando o processo está iniciando ou enquanto ele é executado.

**DML (linguagem de manipulação de dados)**

Essas instruções no SQL que manipulam, em oposição a definir, a dados. Os valores em um banco de dados são selecionados e modificados com DML. Por exemplo, **Inserir**, **Atualizar**, **Excluir**e **Selecione** são instruções SQL DML.

**provedor de documento de origem**

Uma classe especial de provedores que gerenciam documentos e pastas. Quando um documento é representado por um objeto **Record** , ou uma pasta de documentos é representada por um objeto **Recordset** , o provedor de origem do documento preenche esses objetos com um conjunto exclusivo de campos que descrevem as características de um documento, em vez do real do documento em si. Consulte também o **registro de recurso**.

**DSN (nome de fonte de dados)**

A coleção de informações usadas para conectar seu aplicativo para um determinado banco de dados ODBC. O Gerenciador de Driver ODBC usa essas informações para criar uma conexão ao banco de dados. Um DSN pode ser armazenado em um arquivo (um arquivo DSN) ou no registro do Windows (uma máquina DSN).

**propriedade dinâmica**

Uma propriedade específica para um provedor de dados ou o serviço de cursor. A coleção de **Propriedades** de um objeto é preenchida automaticamente com essas ("dinamicamente"). Um objeto não tem nenhuma propriedades dinâmicas até que ele esteja conectado a uma fonte de dados através de um provedor de dados específica. Consulte também o **provedor de dados**, **cursor**.

Retornar ao início

## <a name="e-i"></a>F-I

**enumeração**

Uma lista de constantes nomeadas. Valores enumerados não precisam ser exclusivos. No entanto, o nome de cada valor deve ser exclusivo dentro do escopo em que a enumeração é definida. No ADO, enumerações são usadas para o parâmetro numérico em retornam valores, para adicionar o significado para código ADO e protegem o desenvolvedor contra os valores numéricos (que pode ser alterada de versão para versão). Por exemplo, para abrir um **Recordset**estático, use o valor de **adOpenStatic** enumeradas:  
  

Também conhecido como *enumerado constante*. Consulte também **constante**.

**evento**

Uma ação reconhecida por um objeto para o qual você pode escrever código para responder. Eventos podem ser gerados pela execução do comando, a conclusão da transação, navegação de recordset e atualizações de dados, entre outras ações. Consulte também o **manipulador de eventos**.

**manipulador de eventos**

Um manipulador de eventos é o código que é executado quando um evento ocorre. Consulte também **evento**.

**handler**

Uma rotina que gerencia uma operação, como o gerenciamento de dados ou recuperação de erro ou condição comuns e relativamente simple.

**Recordset hierárquico**

Um **Recordset** que contém outro **conjunto de registros**. Consulte também **data shaping**, **capítulo**.

Para obter mais informações, consulte [Acessando linhas em um Recordset hierárquico](accessing-rows-in-a-hierarchical-recordset.md)

**hierarquia**

Em geral, uma hierarquia é uma estrutura classificada com um superior nível e níveis subordinados. No ADO, hierárquicos **Recordsets** são usados para representar a relação de pai-filho entre um registro e um capítulo. Também no ADO, os objetos **Record** e **Stream** podem ser usados para acessar as estruturas de árvore hierárquica como uma pasta e documentos. ADO MD também inclui a **hierarquia** de objetos para representar uma relação entre os níveis de uma dimensão em um cubo OLAP. Consulte também **objetos Recordset hierárquicos**, **relação pai-filho**, o **capítulo**, a **árvore**.

**ISAPI (Interface de programação de aplicativo de servidor da Internet)**

Um conjunto de funções para os servidores de Internet, como um Windows NT Server/Windows 2000 Server executando o Microsoft Internet Information Services (IIS).

Retornar ao início

## <a name="k-m"></a>K-M

**chave**

Uma coluna ou colunas em uma tabela que identificam exclusivamente uma linha; frequentemente usado para indexar uma tabela.

**empacotamento**

O processo de compactação, envio e descompactação parâmetros de método de interface entre limites de thread ou processo.

**camada intermediária**

A camada lógica em um sistema distribuído entre um cliente de web ou de interface do usuário e o banco de dados. Esse é normalmente onde os objetos comerciais são criados. A camada intermediária é uma coleção de regras comerciais e funções que geram e operam ao receber informações. Realiza isso por meio de regras de negócios, que podem mudar com frequência e, portanto, são encapsuladas em vários componentes que são fisicamente separados da própria lógica do aplicativo. Também conhecido como *camada do servidor de aplicativo*. Consulte também **application distribuído**, a **camada do cliente**, a **camada de fonte de dados**.

**MIME (várias finalidades Internet Mail Extension)**

Um protocolo Internet originalmente desenvolvido para permitir a troca de mensagens de email com conteúdo de rich em rede heterogêneo, máquina e ambientes de email. Na prática, MIME também foi adotado e estendido por aplicativos não sejam de email.

MIME é um padrão que permite que os dados binários ser publicado e ler na Internet. O cabeçalho de um arquivo com dados binários contém o tipo MIME dos dados; Isso informa programas cliente (web navegadores e pacotes de email, por exemplo) que eles precisam lidar com os dados de forma diferente que eles manipulam texto reto. Por exemplo, o cabeçalho de um documento da web que contém uma imagem JPEG contém o tipo MIME específico para o formato de arquivo JPEG. Isso permite que um navegador exibir o arquivo com seu visualizador JPEG, caso haja algum.

Retornar ao início

## <a name="n-o"></a>N-O.

**nó**

Um elemento em uma estrutura de árvore hierárquica. Um nó pode ser raiz ou filho de outro nó. Um nó também pode ser o pai de vários filhos. Consulte também **hierarquia**, **árvore**, **raiz**, **filho**, **pai**.

**variável de objeto**

Uma variável que contém uma referência para um objeto. Por exemplo, objCustomObject é uma variável que aponta para um objeto do tipo ObjetoPersonalizado:  
  
é uma variável que aponta para um objeto do tipo ObjetoPersonalizado:  
  
Definir objCustomObject = CreateObject (adodb. Recordset)

**ODBC (Open Database Connectivity)**

Language interface de programação padrão usada para conectar a uma variedade de fontes de dados. Geralmente, isso é acessado no painel de controle, onde os nomes de fonte de dados (DSNs) podem ser atribuídos aos use drivers ODBC específicos.

**OLE DB**

Um conjunto de interfaces que expor os dados de uma variedade de fontes usando COM. Interfaces do OLE DB fornecem aplicativos com uniform acesso aos dados armazenados em fontes diferentes de informações. Estas interfaces suportam a quantidade de funcionalidade do DBMS apropriada para a fonte de dados, permitindo que ele compartilhar seus dados. Consulte também **COM**.

**bloqueio otimista**

Um tipo de bloqueio em que a página de dados que contém um ou mais registros, inclusive o registro que está sendo editado, está indisponível para outros usuários somente enquanto o registro está sendo atualizado pelo método **Update** , mas está disponível antes e após a chamada para **atualização** .

Proteção otimista é usada quando o objeto **Recordset** for aberto com o parâmetro **LockType** ou a propriedade definida como **adLockOptimistic** ou **adLockBatchOptimistic**. Consulte também **pessimista**.

**valor ordinal**

A posição numérica de um item em um pedido. Em um conjunto do ADO, o valor ordinal do primeiro item é zero (0). O próximo item é um (1) e assim por diante.

Retornar ao início

## <a name="p"></a>P

**comando parametrizado**

Uma consulta ou o comando que permite que você defina os valores de parâmetro antes que o comando é executado. Por exemplo, uma cadeia de caracteres SQL pode ser parametrizada incorporando marcadores de parâmetro na cadeia de caracteres SQL (designados pelo '?' caracteres). O aplicativo, em seguida, especifica valores para cada parâmetro e executa o comando.

**pai**

O lado de controle de uma relação hierárquica. Em uma estrutura hierárquica, um pai tem um ou mais nós filho diretamente abaixo na hierarquia. Consulte também **pai-alias**, **relação pai-filho**, **filho**.

**parent-alias**

Um alias que se refere ao pai. Consulte também **alias**, **pai**.

**relação pai-filho**

Uma relação em uma estrutura hierárquica em que o pai é um nível superior e diretamente associado a um ou mais filhos. Um filho é um nível inferior e deve ter um pai. Consulte também **pai**, **filho**.

**persistência**

Para salvar os dados em um estado permanente, como salvar um **Recordset** em um arquivo.

**bloqueio pessimista**

Um tipo de bloqueio em que a página que contém um ou mais registros, inclusive o registro que está sendo editado, está indisponível para outros usuários para garantir que será feita uma atualização. Comportamento de bloqueio pessimista é definido pelo provedor OLE DB. Normalmente, os registros estão protegidos após a edição e permanecem indisponíveis até que o método de **atualização** foi concluída.

Proteção pessimista é habilitada quando o objeto **Recordset** for aberto com o parâmetro **LockType** ou a propriedade definido como **adLockPessimistic**. Consulte também **bloqueio otimista**.

**pooling**

Uma otimização de desempenho baseada no uso de conjuntos de recursos alocados previamente, como objetos ou conexões de banco de dados. É mais eficiente para desenhar um recurso existente do pool que criar um novo recurso.

**ProgID (identificador programático)**

Um nome exclusivo mapeado no registro do Windows por um aplicativo COM. O ProgID para uma Conexão ADO é "ADODB. Conexão". Consulte também **CLSID**, **COM**.

**proxy**

Um objeto específico de interface que fornece o parâmetro empacotamento e da comunicação necessárias para um cliente chamar um objeto application que está executando em um ambiente de execução diferente, como em um segmento diferente ou em outro processo. O proxy está localizado com o cliente e se comunica com um código correspondente que está localizado com o objeto application que está sendo chamado. Consulte também **stub**.

Retornar ao início

## <a name="r"></a>R

**URL relativa**

Uma URL parcialmente qualificada que especifica um recurso na Internet ou intranet cujo local é em relação ao ponto de partida especificado por uma URL absoluta ou um objeto de Conexão ADO equivalente. Em vigor, o concatenada absoluta e relativa URLs consitute uma URL completa. Consulte também **URL** e a **URL absoluta**.

**fonte de dados remota**

Uma fonte de dados que existe em um outro computador, em vez de no sistema local (onde o aplicativo cliente é executado).

**registro de recurso**

Um registro de um provedor de origem do documento que contém os campos para a definição e a descrição de uma pasta ou um documento. O próprio documento não está contido no registro de recurso, mas normalmente pode ser acessado por um fluxo padrão ou um campo no registro de recurso que contém uma URL. Consulte também o **provedor de origem do documento**, **um fluxo padrão**, **URL**.

**root**

O nível em uma estrutura de árvore hierárquica de superior. O nó raiz tem sem pais, mas pode ter filhos. Consulte também **hierarquia**, **árvore**, **pai**, **filho**.

**conjunto de linhas**

Um conjunto de linhas a partir de uma fonte de dados, tudo tendo o mesmo esquema de campo. Um conjunto de linhas pode representar alguns ou todos os campos de uma tabela. Um conjunto de linhas também pode representar uma tabela virtual, criada por uma consulta ou uma associação de duas ou mais tabelas. No ADO, conjuntos de linhas são representados por objetos **Recordset** .

Retornar ao início

## <a name="s"></a>S

**esquema**

Uma descrição de um banco de dados para o sistema de gerenciamento de banco de dados (DBMS), normalmente gerado usando a linguagem de definição de dados fornecida pelo DBMS. Um esquema define os atributos do banco de dados, como tabelas, colunas e propriedades.

**scope**

O intervalo de referência para um objeto ou variável ou um intervalo de registros em uma tabela ou modo de exibição. Por exemplo, variáveis locais podem ser referidas apenas dentro do procedimento na qual eles foram definidos. Variáveis públicas são acessíveis a partir de qualquer lugar no aplicativo. Objetos, tais como o banco de dados atual, estão no escopo se estiverem no caminho de pesquisa definidas. Intervalos de registro podem ser especificados com uma cláusula de escopo em muitos comandos.

**provedor de serviços**

Software que encapsula um serviço, produzindo e consumindo dados, aumentando recursos em seus aplicativos do ADO. É um provedor que não expõe dados diretamente, em vez disso, ele fornece um serviço, como o processamento de consultas. O provedor de serviços pode processar dados fornecidos pelo provedor de dados. Consulte também o **provedor de dados**.

**Recordset com formato**

Um **Recordset** cujas colunas tenham sido definidas especificamente para conter não apenas dados, mas também referências (chamadas de capítulos) e/ou outros objetos **Recordset** valores computados baseados em outros objetos **Recordset** .

**irmão**

Qualquer dois ou mais nós em uma estrutura hierárquica que estão no mesmo nível na hierarquia. O nó raiz em uma hierarquia não tem nenhuma irmãos.

**procedimento armazenado**

Uma coleção pré-compilado de código como instruções SQL e instruções de controle de fluxo opcionais armazenadas com um nome e processadas como uma unidade. Procedimentos armazenados são armazenados em um banco de dados; eles podem ser executados com uma chamada de um aplicativo e permitem variáveis declaradas por usuário, execução condicional e outros recursos de programação poderosos.

**stub**

Um objeto específico de interface que fornece o parâmetro empacotamento e da comunicação necessárias para um objeto application receber chamadas a partir de um cliente que está executando em um ambiente de execução diferente, como em um segmento diferente ou em outro processo. O fragmento de código está localizado com o objeto application e se comunica com um proxy correspondente que está localizado com o cliente que faz a chamada. Consulte também o **proxy**.

**nó de subsites**

Consulte **filho**.

**operação síncrona**

Uma operação iniciada pelo código que conclui antes da próxima operação pode ser iniciado. Consulte também **operação assíncrona**.

Retornar ao início

## <a name="t-w"></a>T-W

**árvore**

Uma estrutura representando uma relação hierárquica entre elementos (nós). Há um nó de nível superior de uma árvore (a raiz). Sob a raiz, pode haver vários filhos. Cada filho por sua vez pode ser o pai de outros filhos, ramificação assim como uma árvore. Uma pasta que contém documentos e outras pastas é um exemplo típico de uma estrutura de árvore. Consulte também **hierarquia**, **nó**, **raiz**, **filho**, **pai**.

**URL (Uniform Resource Locator)**

Especifica o local de um recurso que residem na Internet ou intranet. Uma URL completa consiste em um esquema (por exemplo, FTP, HTTP, mailto, arquivo e assim por diante), seguido por dois-pontos, um nome de servidor e o caminho completo de um recurso (por exemplo, um documento, gráfico ou outro arquivo). Alguns exemplos de URLs são:  
  
- https://www.domain.com/default.html  
- FTP://FTP.Server.somewhere/FTP.File  
  
- FTP://FTP.Server.somewhere/FTP.File  
- file://Server/Share/File.doc

Consulte também **URL absoluta** e a **URL relativa**.

**servidor Web**

Um computador que fornece serviços da web e páginas para os usuários da Internet e intranet.



