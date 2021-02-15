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

Uma URL totalmente qualificada que especifica o local de um recurso que reside na Internet ou em uma intranet. Consulte também **URL** e **URL relativa.**

**Controle ActiveX**

Auto-registro de componente COM dentro do processo que geralmente tem um elemento visual no tempo de design ou em tempo de executar. Os controles ActiveX também têm a capacidade de se comunicar com um contêiner do Documento Ativo, como o Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

Uma DLL ISAPI que fornece análise, controle de automação, empacotamento de **Recordset** e empacotamento MIME. O componente ADISAPI funciona por meio da API fornecida pelos Serviços de Informações da Internet (IIS). Consulte também **ISAPI**.

**função de agregação**

Em uma consulta, uma função como COUNT, AVG ou STDEV que calcula um valor usando todas as linhas em uma coluna de uma tabela. Ao escrever expressões e programar, você pode usar funções agregadas do SQL (incluindo as três listadas acima) e funções agregadas de domínio para determinar várias estatísticas.

**alias**

Um nome alternativo que você dá a uma coluna ou expressão em uma instrução SQL SELECT, geralmente mais curto ou mais significativo. Por exemplo, BobSales é o alias na seguinte instrução SELECT: "Select wr-Sales as BobSales from SalesDB". Um alias pode ser usado para atribuir dinamicamente colunas para controlar associações no **objeto DataControl** .

**threading de apartment**

Um modelo de threading COM em que todas as chamadas para um objeto ocorrem em um thread. No threading de apartment, COM sincroniza e empacota chamadas. Consulte também **COM**.

**operação assíncrona**

Uma operação que retorna o controle para o programa de chamada sem aguardar a conclusão da operação. Antes que a operação seja concluída, a execução do código continua. Consulte também **a operação síncrona.**

Retornar ao início

## <a name="b"></a>B

**entrada de associação**

Um mapeamento entre um campo em uma tabela e uma variável. Nas extensões do ADO Visual C++, os **campos do Recordset** são mapeados para variáveis C/C++.

**bitmask**

Um valor numérico destinado a uma comparação de valor bit a bit com outros valores numéricos, geralmente para sinalizar opções em valores de parâmetro ou de retorno. Geralmente, essa comparação é feita com operadores lógicos bit a bit, como **And** **e Or** no Visual Basic e **&** em **|** C++.

Por exemplo, os valores **fieldAttributeEnum** do ADO podem ser usados como bitmasks para determinar os atributos de um campo. Suponha que você quisesse determinar se um campo era atualizável. Você pode testar isso com a expressão a seguir no Visual Basic:  
  

Se o resultado for VERDADEIRO, o campo será atualizável.

**bookmark**

Um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas para que um usuário possa navegar rapidamente até ela.

**objeto de negócios**

Um objeto que executa um conjunto definido de operações, como validação de dados ou lógica de regra comercial. Os objetos de negócios geralmente residem na camada intermediária.

**regra comercial**

A combinação de edições de validação, verificações de logon, verificações de banco de dados, políticas e transformações de algoritmos que constituem o modo de fazer negócios de uma empresa. Também conhecido como *lógica de negócios.*

Retornar ao início

## <a name="c"></a>C

**calculated expression**

Uma expressão que não é constante, mas cujo valor depende de outros valores. Para ser avaliada, uma expressão calculada deve obter e calcular valores de outras fontes, normalmente em outros campos ou linhas.

**capítulo**

Uma referência a um intervalo de linhas de uma fonte de dados. No ADO, um capítulo é normalmente uma referência a outro **Recordset.**

As colunas de capítulo permitem definir uma relação *parent-child* em que *parent* representa o **Recordset** contendo a coluna de capítulo, e *child* é o **Recordset** representado pelo capítulo.

**chapter-alias**

Um alias que se refere à coluna anexada ao pai.

**conjunto de caracteres**

Um mapeamento de um conjunto de caracteres para seus valores numéricos. Por exemplo, Unicode é um conjunto de caracteres de 16 bits capaz de codificar todos os caracteres conhecidos e usado como um padrão mundial de codificação de caracteres.

**filho**

O lado dependente de uma relação hierárquica. Um filho é um nó em uma estrutura hierárquica que tem outro nó acima dele (mais próximo da raiz). Consulte também **child-alias**, **relação pai-filho**, **pai**.

**child-alias**

Um alias que se refere ao filho. Consulte também **alias**, **filho**.

**CLSID (identificador de classe)**

Um identificador universal exclusivo (UUID) que identifica um componente COM. Cada componente COM tem seu CLSID no Registro do Windows para que possa ser carregado por outros aplicativos. Consulte também **ProgID**, **COM**.

**camada do cliente**

Uma camada lógica de um sistema distribuído que normalmente apresenta dados e processa a entrada do usuário, às vezes chamado de *front-end.* Normalmente, a camada do cliente solicita dados de um servidor com base na entrada e, em seguida, formatar e exibir o resultado. Consulte também camada **intermediária**, **camada de fonte de dados**, aplicativo **distribuído**.

**COM (Component Object Model)**

Um padrão binário que permite que objetos interoperem em um ambiente em rede, independentemente do idioma em que foram desenvolvidos ou em quais computadores residem. Tecnologias baseadas em COM incluem Controles ActiveX, Automação e vinculação e incorporação de objetos (OLE). O COM permite que um objeto exponha sua funcionalidade a outros componentes e hospede aplicativos. Ele define como o objeto se expõe e como essa exposição funciona em processos e em redes. COM também define o ciclo de vida do objeto.

**Componente COM**

Arquivo binário — como .dll, .ocx e alguns arquivos .exe — que oferece suporte ao padrão COM para fornecer objetos. Esse arquivo contém código para uma ou mais armas de classe, classes COM, mecanismos de entrada do Registro, código de carregamento e assim por diante.

**operador de comparação**

Um operador que compara duas expressões e retorna um valor booleano.

Um parâmetro de critério que pode ser expresso como " \> " (maior que), \< " " (menor que), "=" (igual), " \> =" (maior ou igual), " \< =" (menor ou igual), \< \> " " (diferente) ou "like" (correspondência de padrão).

**component**

Um objeto que encapsula dados e códigos e fornece um conjunto bem especificado de serviços publicamente disponíveis.

**arquivo composto**

Uma implementação de armazenamento estruturado com COM para arquivos. Um arquivo composto armazena objetos separados em um único arquivo estruturado que consiste em dois elementos principais: objetos de armazenamento e objetos de fluxo. Juntos, eles funcionam como um sistema de arquivos em um arquivo. Para obter mais informações, consulte Arquivos Compostos no SDK da Plataforma Microsoft.

Vários arquivos individuais vinculados em um arquivo físico. Cada arquivo individual em um arquivo composto pode ser acessado como se fosse um único arquivo físico.

**constante**

Um valor numérico ou de cadeia de caracteres que não muda. Enumerações do ADO nomeadas (constantes enumeradas) podem ser usadas em seu código em vez de valores reais, por exemplo, **adUseClient** é uma constante cujo valor é 3. (Const adUseClient = 3). Consulte também **enumeração**.

**cursor**

Um elemento de banco de dados que controla a navegação de registros, a capacidade de atualização de dados e a visibilidade das alterações feitas no banco de dados por outros usuários.

Retornar ao início

## <a name="d"></a>D

**vinculação de dados**

O processo de associação dos objetos ou controles de um aplicativo a uma fonte de dados. Um controle associado a uma fonte de dados é chamado de controle *vinculado a dados.*

O conteúdo de um controle vinculado a dados está associado a valores de um banco de dados. Por exemplo, um controle de grade vinculado a um objeto **Recordset** pode ser atualizado quando as linhas do **Recordset** são atualizadas. Quando novos valores são recuperados pelo **Recordset,** novos valores são exibidos na grade.

**provedor de dados**

Software que expõe dados a um aplicativo ADO diretamente ou por meio de um provedor de serviços. Consulte também provedor **de serviços.**

**data shaping**

Uma técnica que faz uso de uma sintaxe formalizada (chamada de linguagem **Shape)** para definir um objeto **Recordset** especializado (chamado de **Recordset** com formato) que contém não apenas dados, mas também referências a outros objetos **Recordset** e/ou valores calculados com base nesses outros objetos **Recordset.**

**camada de fonte de dados**

Uma camada lógica de um sistema distribuído que representa um computador executando um DBMS, como um banco de dados do SQL Server. Consulte também a **camada do cliente,** **camada intermediária,** **aplicativo distribuído.**

**DCOM**

Um protocolo de transmissão que permite que os componentes COM se comuniquem diretamente uns com os outros em uma rede. Consulte também **COM**, **componente**.

**DDL (Linguagem de Definição de Dados)**

As instruções no SQL que definem, em vez de manipular, dados. O esquema de um banco de dados é criado ou modificado com DDL. Por exemplo, **CREATE TABLE**, **CREATE INDEX**, **GRANT** e **REVOKE são** instruções DDL sql.

**fluxo padrão**

Um fluxo de texto ou binário (representado por um objeto **Stream)** que é associado a objetos **Record** ou **Recordset** ao usar determinados provedores OLE DB, como o Microsoft OLE DB Provider for Internet Publishing. O fluxo padrão normalmente contém o conteúdo de um arquivo, como o código HTML para a raiz de um site.

**aplicativo distribuído**

Um programa escrito para que o processamento possa ser dividido entre vários computadores em uma rede. Normalmente, um aplicativo distribuído é dividido em apresentação, lógica de negócios e camadas de armazenamento de dados ou *camadas.* Consulte também a **camada do cliente**, camada **intermediária**, camada de fonte **de dados.**

**Recordset desconectado**

Um **objeto Recordset** em um cache de cliente que não tem mais uma conexão ao vivo com o servidor. Se a fonte de dados original precisar ser acessada novamente por algum motivo, como atualizar dados, a conexão deverá ser estabelecida novamente. No entanto, as coleções, as propriedades e os métodos de um **Recordset** desconectado ainda podem ser acessados.

**DLL (biblioteca de vínculo dinâmico)**

Um arquivo que contém uma ou mais funções compiladas, vinculadas e armazenadas separadamente dos processos que as utilizam. O sistema operacional mapeia as DLLs para o espaço de endereço do processo de chamada quando o processo é iniciando ou enquanto ele está em execução.

**DML (Linguagem de Manipulação de Dados)**

As instruções no SQL que manipulam, em vez de definir, dados. Os valores em um banco de dados são selecionados e modificados com DML. Por exemplo, **INSERT**, **UPDATE,** **DELETE** e **SELECT são** instruções DML sql.

**provedor de fonte de documentos**

Uma classe especial de provedores que gerenciam pastas e documentos. Quando um documento é representado por um objeto **Record** ou uma pasta de documentos é representada por um objeto **Recordset,** o provedor de origem do documento preenche esses objetos com um conjunto exclusivo de campos que descrevem características do documento, em vez do próprio documento real. Consulte também o **registro de recursos.**

**DSN (nome da fonte de dados)**

A coleção de informações usadas para conectar seu aplicativo a um banco de dados ODBC específico. O Gerenciador de Driver ODBC usa essas informações para criar uma conexão com o banco de dados. Um DSN pode ser armazenado em um arquivo (um arquivo DSN) ou no Registro do Windows (um DSN de computador).

**propriedade dinâmica**

Uma propriedade específica de um provedor de dados ou do serviço de cursor. A **coleção Properties** de um objeto é preenchida com elas automaticamente ("dinamicamente"). Um objeto não tem propriedades dinâmicas até que esteja conectado a uma fonte de dados por meio de um provedor de dados específico. Consulte também **o provedor de dados**, **cursor**.

Retornar ao início

## <a name="e-i"></a>E-I

**enumeração**

Uma lista de constantes nomeadas. Os valores enumerados não precisam ser exclusivos. No entanto, o nome de cada valor deve ser exclusivo dentro do escopo onde a enumeração é definida. No ADO, as enumerações são usadas para parâmetro numérico e valores de retorno, para adicionar significado ao código do ADO e para proteger o desenvolvedor dos valores numéricos (que podem mudar de uma versão para outra). Por exemplo, para abrir um **Recordset estático,** use o valor enumerado **adOpenStatic:**  
  

Também conhecido como constante *enumerada*. Consulte também **constante**.

**evento**

Uma ação reconhecida por um objeto, para a qual você pode escrever código para responder. Os eventos podem ser gerados por execução de comando, conclusão de transação, navegação de recordset e atualizações de dados, entre outras ações. Consulte também o **manipulador de eventos.**

**manipulador de eventos**

Um manipulador de eventos é o código que é executado quando ocorre um evento. Consulte também **evento**.

**handler**

Uma rotina que gerencia uma condição ou operação comum e relativamente simples, como recuperação de erros ou gerenciamento de dados.

**Recordset hierárquico**

Um **Recordset** que contém outro **Recordset**. Consulte também **data shaping**, **capítulo**.

Para obter mais informações, [consulte Acessando linhas em um recordset hierárquico](accessing-rows-in-a-hierarchical-recordset.md)

**hierarchy**

Em geral, uma hierarquia é uma estrutura classificada com níveis de nível superior e subordinados. No ADO, **recordsets** hierárquicos são usados para representar a relação pai-filho entre um registro e um capítulo. Também no ADO, os **objetos Record** e **Stream** podem ser usados para acessar estruturas de árvore hierárquicas, como uma pasta e documentos. O ADO MD também inclui **objetos Hierarchy** para representar uma relação entre os níveis de uma dimensão em um cubo OLAP. Consulte também **recordsets hierárquicos**, **relação pai-filho**, **capítulo**, **árvore**.

**ISAPI (Internet Server Application Programming Interface)**

Um conjunto de funções para servidores de Internet, como um Windows NT Server/Windows 2000 Server executando o Microsoft Internet Information Services (IIS).

Retornar ao início

## <a name="k-m"></a>K-M

**key**

Uma coluna ou colunas em uma tabela que identificam exclusivamente uma linha; frequentemente usado para indexar uma tabela.

**marshaling**

O processo de empacotamento, envio e descompactação de parâmetros do método de interface entre limites de thread ou processo.

**camada intermediária**

A camada lógica em um sistema distribuído entre uma interface do usuário ou um cliente Web e o banco de dados. Normalmente, é aqui que os objetos de negócios são instaciados. A camada intermediária é um conjunto de regras e funções de negócios que geram e operam ao receber informações. Eles fazem isso por meio de regras de negócios, que podem mudar com frequência e, portanto, são encapsuladas em componentes que são fisicamente separados da lógica do aplicativo em si. Também conhecido como camada *de servidor de aplicativos.* Consulte também **aplicativo distribuído, camada do** **cliente**, camada de fonte **de dados**.

**MIME (Extensão de Email da Internet multiuso)**

Um protocolo de Internet originalmente desenvolvido para permitir a troca de mensagens de email com conteúdo rico em ambientes heterogêneos de rede, computador e email. Na prática, o MIME também foi adotado e estendido por aplicativos que não são de email.

MIME é um padrão que permite que dados binários sejam publicados e lidos na Internet. O header de um arquivo com dados binários contém o tipo MIME dos dados; Isso informa aos programas cliente (navegadores da Web e pacotes de email, por exemplo) que eles precisarão lidar com os dados de maneira diferente do que lidar com texto reto. Por exemplo, o header de um documento da Web que contém um gráfico JPEG contém o tipo MIME específico para o formato de arquivo JPEG. Isso permite que um navegador exibir o arquivo com seu visualizador JPEG, se um estiver presente.

Retornar ao início

## <a name="n-o"></a>N-O

**node**

Um elemento em uma estrutura de árvore hierárquica. Um nó pode ser a raiz ou o filho de outro nó. Um nó também pode ser pai de vários filhos. Consulte também **hierarquia**, **árvore**, **raiz**, **filho**, **pai**.

**variável de objeto**

Uma variável que contém uma referência para um objeto. Por exemplo, objCustomObject é uma variável que aponta para um objeto do tipo CustomObject:  
  
é uma variável que aponta para um objeto do tipo CustomObject:  
  
Set objCustomObject = CreateObject(adodb. Recordset)

**ODBC**

Uma interface de linguagem de programação padrão usada para se conectar a uma variedade de fontes de dados. Isso geralmente é acessado por meio do Painel de Controle, onde nomes de fonte de dados (DSNs) podem ser atribuídos para usar drivers ODBC específicos.

**OLE DB**

Um conjunto de interfaces que expõem dados de uma variedade de fontes usando COM. As interfaces OLE DB fornecem aplicativos com acesso uniforme a dados armazenados em diversas fontes de informações. Essas interfaces suportam a quantidade de funcionalidade DBMS apropriada à fonte de dados, permitindo que ela compartilhe seus dados. Consulte também **COM**.

**bloqueio otimista**

Um tipo de bloqueio no qual a página de dados que contém um ou mais registros, incluindo o registro que está sendo editado, está indisponível para outros usuários somente enquanto o registro está sendo atualizado pelo método **Update,** mas está disponível antes e depois da chamada para **Atualizar.**

Bloqueio otimista é usado quando o objeto **Recordset** é aberto com o parâmetro **LockType** ou a propriedade definida como **adLockOptimistic** ou **adLockBatchOptimistic**. Consulte também **o bloqueio pessimista.**

**valor ordinal**

O local numérico de um item dentro de um pedido. Em uma coleção ADO, o valor ordinal do primeiro item é zero (0). O próximo item é um (1) e assim por diante.

Retornar ao início

## <a name="p"></a>P

**comando parametrizado**

Uma consulta ou comando que permite definir valores de parâmetro antes de o comando ser executado. Por exemplo, uma cadeia de caracteres SQL pode ser parametrizada pela incorporação de marcadores de parâmetro na cadeia de caracteres SQL (designada pelo caractere '?'). Em seguida, o aplicativo especifica valores para cada parâmetro e executa o comando.

**primário**

O lado de controle de uma relação hierárquica. Em uma estrutura hierárquica, um pai tem um ou mais nós filho diretamente abaixo dela na hierarquia. Consulte também **parent-alias**, **parent-child relationship**, **child**.

**parent-alias**

Um alias que se refere ao pai. Consulte também **alias**, **pai**.

**relação pai-filho**

Uma relação em uma estrutura hierárquica na qual o pai é um nível superior e associado diretamente a um ou mais filhos. Um filho está um nível mais baixo e deve ter um pai. Consulte também **pai**, **filho**.

**persist**

Para salvar dados em um estado permanente, como salvar um **Recordset** em um arquivo.

**bloqueio pessimista**

Um tipo de bloqueio no qual a página que contém um ou mais registros, incluindo o registro que está sendo editado, não está disponível para outros usuários para garantir que uma atualização será feita. O comportamento de bloqueio pessimista é definido pelo provedor OLE DB. Normalmente, os registros são bloqueados na edição e permanecem indisponíveis até que **o método Update** seja concluído.

O bloqueio pessimista é habilitado quando o objeto **Recordset** é aberto com o parâmetro **LockType** ou a propriedade definida como **adLockPessimistic**. Veja também **bloqueio otimista.**

**pooling**

Uma otimização de desempenho baseada no uso de coleções de recursos pré-alocados, como objetos ou conexões de banco de dados. É mais eficiente desenhar um recurso existente do pool do que criar um novo recurso.

**ProgID (identificador programático)**

Um nome exclusivo mapeado para o Registro do Windows por um aplicativo COM. O ProgID de uma conexão do ADO é "ADODB. Connection". Consulte também **CLSID**, **COM**.

**proxy**

Um objeto específico da interface que fornece o empacotamento do parâmetro e a comunicação necessária para um cliente chamar um objeto de aplicativo que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo. O proxy está localizado com o cliente e se comunica com um stub correspondente que está localizado com o objeto de aplicativo que está sendo chamado. Consulte também **stub**.

Retornar ao início

## <a name="r"></a>R

**URL relativa**

Uma URL parcialmente qualificada que especifica um recurso na Internet ou em uma intranet cujo local é relativo a um ponto de partida especificado por uma URL absoluta ou um objeto connection do ADO equivalente. Na verdade, as URLs absolutas e relativas concatenadas restringem uma URL completa. Consulte também **URL** e **URL absoluta.**

**fonte de dados remota**

Uma fonte de dados que existe em outro computador, e não no sistema local (onde o aplicativo cliente é executado).

**registro de recurso**

Um registro de um provedor de fonte de documentos que contém campos para a definição e a descrição de uma pasta ou documento. O próprio documento não está contido no registro de recursos, mas normalmente pode ser acessado pelo fluxo padrão ou por um campo no registro de recursos que contém uma URL. Consulte também o **provedor de origem do documento,** **fluxo padrão,** **URL**.

**root**

O nível superior em uma estrutura de árvore hierárquica. O nó raiz não tem pais, mas pode ter filhos. Consulte também **hierarquia**, **árvore**, **pai**, **filho**.

**rowset**

Um conjunto de linhas de uma fonte de dados, todas com o mesmo esquema de campo. Um rowset pode representar todos ou alguns campos de uma tabela. Um rowset também pode representar uma tabela virtual, criada por uma consulta ou uma junção de duas ou mais tabelas. No ADO, os conjuntos de linhas são representados por **objetos Recordset.**

Retornar ao início

## <a name="s"></a>S

**schema**

Uma descrição de um banco de dados para o dbMS (sistema de gerenciamento de banco de dados), normalmente gerado usando o idioma de definição de dados fornecido pelo DBMS. Um esquema define atributos do banco de dados, como tabelas, colunas e propriedades.

**scope**

O intervalo de referência para um objeto ou variável ou um intervalo de registros em uma exibição ou tabela. Por exemplo, as variáveis locais podem ser referenciadas somente dentro do procedimento em que foram definidas. As variáveis públicas podem ser acessadas de qualquer lugar no aplicativo. Objetos, como o banco de dados atual, estão no escopo se eles estão no caminho de pesquisa definido. Os intervalos de registros podem ser especificados com uma cláusula Scope em muitos comandos.

**provedor de serviços**

Software que encapsula um serviço produzindo e consumindo dados, aumentando os recursos em seus aplicativos ADO. É um provedor que não expõe dados diretamente, em vez disso, fornece um serviço, como o processamento de consultas. O provedor de serviços pode processar dados fornecidos por um provedor de dados. Consulte também o **provedor de dados.**

**Recordset com formato**

Um **Recordset** cujas colunas foram especificamente definidas para conter não apenas dados, mas também referências (chamadas de capítulos) a outros objetos **Recordset** e/ou valores calculados com base em outros objetos **Recordset.**

**sibling**

Qualquer dois ou mais nós em uma estrutura hierárquica que estão no mesmo nível na hierarquia. O nó raiz em uma hierarquia não tem irmãos.

**procedimento armazenado**

Uma coleção pré-compilada de código, como instruções SQL e instruções opcionais de controle de fluxo armazenadas em um nome e processadas como uma unidade. Os procedimentos armazenados são armazenados em um banco de dados; eles podem ser executados com uma chamada de um aplicativo e permitir variáveis declaradas pelo usuário, execução condicional e outros recursos avançados de programação.

**stub**

Um objeto específico da interface que fornece o empacotamento do parâmetro e a comunicação necessária para que um objeto de aplicativo receba chamadas de um cliente que está sendo executado em um ambiente de execução diferente, como em um thread diferente ou em outro processo. O stub está localizado com o objeto application e se comunica com um proxy correspondente que está localizado com o cliente que o chama. Consulte também **proxy**.

**sub-nó**

Ver **filho**.

**operação síncrona**

Uma operação iniciada pelo código que é concluída antes do início da próxima operação. Consulte também **a operação assíncrona.**

Retornar ao início

## <a name="t-w"></a>T-W

**árvore**

Uma estrutura que representa uma relação hierárquica entre elementos (nós). Há um nó no nível superior de uma árvore (a raiz). Sob a raiz, pode haver vários filhos. Cada filho, por sua vez, pode ser pai de outros filhos, ramificando assim como uma árvore. Uma pasta que contém documentos e outras pastas é um exemplo típico de uma estrutura de árvore. See also **hierarchy**, **node**, **root**, **child**, **parent**.

**URL (Uniform Resource Locator)**

Especifica a localização de um recurso que reside na Internet ou em uma intranet. Uma URL completa consiste em um esquema (como FTP, HTTP, mailto, arquivo e assim por diante), seguido por dois pontos, um nome de servidor e o caminho completo de um recurso (como um documento, gráfico ou outro arquivo). Alguns exemplos de URLs são:  
  
- https://www.domain.com/default.html  
- ftp://ftp.server.somewhere/ftp.file  
  
- ftp://ftp.server.somewhere/ftp.file  
- file://Server/Share/File.doc

Consulte também **a URL absoluta** e a URL **relativa.**

**servidor Web**

Um computador que fornece serviços Web e páginas para usuários da intranet e da Internet.



