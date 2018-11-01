---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66ef27165e6f5823cc97a295643dfc2ae5c205c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883180"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB Provider for ODBC

**Aplica-se a**: Access 2013, o Office 2013

Para um programador de ADO ou RDS, o mundo ideal seria aquele em que todas as fontes de dados apresentassem uma interface OLE DB, de modo que as chamadas do ADO pudessem ser feitas diretamente na fonte de dados. Embora cada vez mais fornecedores de bancos de dados venham implementando interfaces OLE DB, algumas fontes de dados ainda não são expostas dessa maneira. Por outro lado, praticamente todos os sistemas DBMS em uso hoje em dia podem ser acessados por ODBC.

Já existem drivers ODBC disponíveis para todos os principais DBMS em uso atualmente, incluindo Microsoft SQL Server, Microsoft Access (mecanismo de banco de dados do Microsoft Jet) e Microsoft FoxPro, além de produtos de banco de dados produzidos por outro fornecedor, como a Oracle.

Entretanto, o Microsoft ODBC Provider permite a conexão do ADO com qualquer fonte de dados ODBC. O provedor é de encadeamento livre e habilitado para Unicode.

O provedor oferece suporte a transações, embora diferentes mecanismos DBMS ofereçam diferentes tipos de suporte a transações. Por exemplo, o Microsoft Access oferece suporte a transações aninhadas com até cinco níveis de profundidade.

Esse é o provedor padrão para o ADO, oferecendo suporte a todas propriedades e métodos do ADO dependentes de provedor.

## <a name="connection-string-parameters"></a>Parâmetros da sequência de conexão

Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```sql 
 
MSDASQL 
```

A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.

## <a name="typical-connection-string"></a>Sequência de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

A cadeia de caracteres consiste nas seguintes palavras-chave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palavra-chave</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica o OLE DB Provider for ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>DSN</strong></p></td>
<td><p>Especifica o nome da fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UID</strong></p></td>
<td><p>Especifica o nome do usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>Especifica a senha do usuário.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL</strong></p></td>
<td><p>Especifica a URL de um arquivo ou diretório publicado em uma pasta da web.</p></td>
</tr>
</tbody>
</table>


Como esse é o provedor padrão para o ADO, se você omitir o parâmetro **Provider=** na sequência de conexão, o ADO tentará estabelecer uma conexão com esse provedor.

Embora não ofereça suporte a quaisquer parâmetros específicos de conexão além dos definidos pelo ADO, o provedor passará quaisquer parâmetros de conexão não-ADO para o gerenciador de driver ODBC.

Como é possível omitir o parâmetro **Provider**, você pode compor uma sequência de conexão ADO que seja idêntica a uma sequência de conexão ODBC para a mesma fonte de dados. Use os mesmos nomes de parâmetros (**DRIVER=**, **DATABASE=**, **DSN=**, e assim por diante), valores e sintaxe que você usaria para compor uma sequência de conexão ODBC. Você pode se conectar com ou sem um nome predefinido de fonte de dados (DSN) ou FileDSN.

**Sintaxe com um DSN ou FileDSN:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Sintaxe sem um DSN (conexão sem DSN):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Se você usar um **DSN** ou **FileDSN**, é necessário que ele seja definido com o Administrador de Fonte de Dados ODBC no Painel de Controle do Windows. No Microsoft Windows 2000, o Administrador ODBC está localizado nas Ferramentas Administrativas. Em versões anteriores do Windows, o ícone do Administrador ODBC era denominado **ODBC de 32 bits** ou simplesmente **ODBC**.

Uma alternativa à definição de um **DSN** seria especificar o driver ODBC (**DRIVER=**), como "SQL Server;", o nome do servidor (**SERVER=**); e o nome do banco de dados (**DATABASE=**).

Você também pode especificar o nome de uma conta de usuário (**UID=**) e a senha dessa conta (**PWD=**) nos parâmetros específicos para ODBC ou nos parâmetros padrão *user* e *password* definidos pelo ADO.

Embora uma definição de **DSN** já especifica um banco de dados, você pode especificar *um* parâmetro de *banco de dados* , além de um **DSN** para se conectar a um banco de dados diferente. É uma boa ideia sempre incluir *o* parâmetro de *banco de dados* quando você usa um **DSN**. Isso garantirá a conexão com o banco de dados apropriado, mesmo que outro usuário tenha alterado o parâmetro referente do banco de dados padrão desde a última vez que você verificou a definição do **DSN**.

## <a name="provider-specific-connection-properties"></a>Parâmetros de conexão específicos para provedor

O provedor OLE DB para ODBC adiciona várias propriedades à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. A tabela abaixo lista essas propriedades, com o nome da propriedade do OLE DB correspondente entre parênteses.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Accessible Procedures<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Indica se o usuário tem acesso a procedimentos armazenados.</p></td>
</tr>
<tr class="even">
<td><p>Tabelas acessíveis<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Indica se o usuário tem permissão para executar instruções SELECT nas tabelas do banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Instruções de ativas<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Indica o número de identificadores aos quais um driver ODBC pode oferecer suporte em uma conexão.</p></td>
</tr>
<tr class="even">
<td><p>Nome do driver<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Indica o nome do arquivo do driver ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Versão do driver ODBC<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Indica a versão do ODBC à qual o driver oferece suporte.</p></td>
</tr>
<tr class="even">
<td><p>Uso de arquivos<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Indica como o driver trata um arquivo em uma fonte de dados; como uma tabela ou como um catálogo.</p></td>
</tr>
<tr class="odd">
<td><p>Escape cláusula LIKE<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Indica se o driver oferece suporte à definição e utilização de um caractere de escape no lugar do caractere de porcentagem (%) e do caractere de sublinhado (_) no predicado LIKE de uma cláusula WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Máximo de colunas no grupo por<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Indica o número máximo de colunas que podem ser listadas na cláusula GROUP BY de uma instrução SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Máximo de colunas no índice<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Indica o número máximo de colunas que podem ser incluídas em um índice.</p></td>
</tr>
<tr class="even">
<td><p>Máximo de colunas por ordem<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Indica o número máximo de colunas que podem ser listadas na cláusula ORDER BY de uma instrução SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Máximo de colunas em Select<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Indica o número máximo de colunas que podem ser listadas na parte SELECT de uma instrução SELECT.</p></td>
</tr>
<tr class="even">
<td><p>Máximo de colunas na tabela<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Indica o número máximo de colunas permitidas em uma tabela.</p></td>
</tr>
<tr class="odd">
<td><p>Funções numéricas<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Indica as funções numéricas às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Recursos de associação externa<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Indica os tipos de junções externas (OUTER JOINs) aos quais o provedor oferece suporte.</p></td>
</tr>
<tr class="odd">
<td><p>Junções externas<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Indica se o provedor oferece suporte a junções externas (OUTER JOINs).</p></td>
</tr>
<tr class="even">
<td><p>Caracteres especiais<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Indica quais caracteres têm um significado especial para o driver ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Procedimentos armazenados<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Indica se há procedimentos armazenados disponíveis para utilização com esse driver ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Funções de sequência<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Indica as funções de cadeia de caracteres às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Funções do sistema<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Indica as funções do sistema às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Funções de data/hora<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Indica as funções de hora e data às quais o driver ODBC oferece suporte. Para obter uma listagem dos nomes de funções e valores associados utilizados nesta máscara de bits, consulte o Apêndice E: funções escalares da documentação do ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Suporte a gramática SQL<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Indica a gramática SQL à qual o driver ODBC oferece suporte.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Propriedades de Recordset e Command específicas para provedor

O provedor OLE DB para ODBC adiciona várias propriedades à coleção **Properties** dos objetos **Recordset** e **Command**. A tabela abaixo lista essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Consultas com base em exclui/atualizações/inserirá<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Indica se atualizações, exclusões e inserções podem ser realizadas utilizando consultas SQL.</p></td>
</tr>
<tr class="even">
<td><p>Tipo de simultaneidade ODBC<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Indica o método utilizado para reduzir problemas potenciais que surgem quando dois usuários tentam acessar simultaneamente os mesmos dados na fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Acessibilidade do BLOB no cursor somente de encaminhamento<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Indica se <strong>Fields</strong> BLOB podem ser acessados quando um cursor somente de encaminhamento estiver sendo utilizado.</p></td>
</tr>
<tr class="even">
<td><p>Incluem valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL em QBU WHERE cláusulas<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Indica se valores SQL_FLOAT, SQL_DOUBLE e SQL_REAL podem ser incluídos em uma cláusula QBU WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>Posição na última linha, após inserir<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Indica que, após a inserção de um novo registro em uma tabela, a última linha da tabela passará a ser a linha atual.</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Indica se a interface <strong>IRowsetChange</strong> oferece suporte a informações estendidas.</p></td>
</tr>
<tr class="odd">
<td><p>Tipo de Cursor ODBC<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Indica o tipo de cursor utilizado pelo <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Gerar um conjunto de linhas que pode ser empacotado.<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Indica que o driver ODBC gera um conjunto de registros que pode ser empacotado.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Texto de comando

A forma de utilização do objeto [Command](command-object-ado.md) depende em grande parte da fonte de dados e dos tipos de consultas e instruções de comando que ela aceita.

O ODBC fornece uma sintaxe específica para chamar procedimentos armazenados. Para a propriedade [CommandText](commandtext-property-ado.md) do argumento *origem* para o método **Open** em um [Recordset](recordset-object-ado.md) , o argumento *CommandText* para o método **Execute** em um objeto de [Conexão](connection-object-ado.md) ou um objeto **Command** objeto, passa em uma cadeia de caracteres com esta sintaxe:

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

Cada **?** faz referência a um objeto na coleção [Parameters](parameters-collection-ado.md). O primeiro **?** faz referência a **Parameters**(0), o segundo **?** a **Parameters**(1), e assim por diante.

As referências a parâmetros são opcionais e dependem da estrutura do procedimento armazenado. Se você quiser chamar um procedimento armazenado que não define qualquer parâmetro, sua cadeia de caracteres será semelhante a esta:

`"{ call procedure }"`

Se você tiver dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:

`"{ call procedure ( ?, ? ) }"`

Se o procedimento armazenado retornar um valor, esse valor de retorno será tratado como outro parâmetro. Se você não tiver parâmetros de consulta, mas tiver um valor de retorno, sua cadeia de caracteres será semelhante a esta:

`"{ ? = call procedure }"`

Finalmente, se você tiver um valor de retorno e dois parâmetros de consulta, sua cadeia de caracteres será semelhante a esta:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Comportamento do Recordset

As tabelas abaixo listam os métodos e propriedades do ADO disponíveis em um objeto **Recordset** aberto com esse provedor.

Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção **Properties** de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.

Disponibilidade das propriedades padrão do **Recordset** do ADO:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriedade</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dinâmico</p></th>
<th><p>Conjunto de chaves</p></th>
<th><p>Estático</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>não disponível</p></td>
<td><p>não disponível</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>não disponível</p></td>
<td><p>não disponível</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>não disponível</p></td>
<td><p>não disponível</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filtrar</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>não disponível</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>não disponível</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Origem</a></p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
<td><p>somente leitura</p></td>
</tr>
</tbody>
</table>


As propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [AbsolutePage](absolutepage-property-ado.md) são somente leitura quando o ADO é utilizado com a versão 1.0 do Microsoft OLE DB Provider for ODBC.

Disponibilidade dos métodos padrão do **Recordset** do ADO:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dinâmico</p></th>
<th><p>Conjunto de chaves</p></th>
<th><p>Estático</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Não</p></td>
<td><p>Não</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Mover</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Não</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Não</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a>*</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Não</p></td>
<td><p>Não</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Suporta</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
<td><p>Sim</p></td>
</tr>
</tbody>
</table>


\*Sem suporte em bancos de dados do Microsoft Access.

## <a name="dynamic-properties"></a>Propriedades dinâmicas

O Microsoft OLE DB Provider for ODBC insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.

As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.

## <a name="connection-dynamic-properties"></a>Propriedades dinâmicas de Connection

As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade do ADO</p></th>
<th><p>Nome da propriedade do OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Connect Timeout</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Extended Properties</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Initial Catalog</p></td>
<td><p>DBPROP_INIT_CATALOG</p></td>
</tr>
<tr class="even">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>Location</p></td>
<td><p>DBPROP_INIT_LOCATION</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Services</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Persist Security Info</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Propriedades dinâmicas do Recordset

As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade do ADO</p></th>
<th><p>Nome da propriedade do OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Unique Rows</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Propriedades dinâmicas do Command

As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade do ADO</p></th>
<th><p>Nome da propriedade do OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

Para obter detalhes sobre a implementação específica e informações funcionais sobre o Microsoft OLE DB Provider for ODBC, consulte o [Guia do programador do OLE DB do](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visite a [Central de desenvolvedores de plataforma de dados](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

