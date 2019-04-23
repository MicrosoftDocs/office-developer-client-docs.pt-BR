---
title: Microsoft OLE DB Provider for Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288922"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a>Provedor Microsoft OLE DB para Microsoft Jet

**Aplica-se ao:** Access 2013, Office 2013

O OLE DB Provider for Microsoft Jet permite que o ADO acesse bancos de dados do Microsoft Jet.

## <a name="connection-string-parameters"></a>Parâmetros da sequência de conexão

Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.

## <a name="typical-connection-string"></a>Sequência de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
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
<td><p>Especifica o OLE DB Provider for Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica o caminho e o nome de arquivo do banco de dados (por exemplo, c:\Northwind.mdb).</p></td>
</tr>
<tr class="odd">
<td><p><strong>ID de usuário</strong></p></td>
<td><p>Especifica o nome de usuário. Se essa palavra-chave não for especificada, a &quot;cadeia&quot;de caracteres, admin, será usada por padrão.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica a senha do usuário. Se essa palavra-chave não for especificada, a cadeia&quot;&quot;de caracteres vazia () será usada por padrão.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Parâmetros de conexão específicos para provedor

O OLE DB Provider for Microsoft Jet oferece suporte a várias propriedades dinâmicas específicas para o provedor, além daquelas definidas pelo ADO. Como ocorre com todos os demais parâmetros **Connection**, estes podem ser definidos por meio da coleção **Properties** do objeto **Connection** ou como parte da sequência de conexão.

A tabela abaixo relaciona essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Jet OLEDB: quantidade de espaço em estado de recuperação<br />
(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</p></td>
<td><p>Indica uma estimativa da quantidade de espaço, em bytes, que pode ser recuperada compactando-se o banco de dados. Esse valor é válido somente depois que uma conexão com o banco de dados tiver sido estabelecida.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: controle de conexão<br />
(DBPROP_JETOLEDB_CONNECTIONCONTROL)</p></td>
<td><p>Indica se os usuários podem se conectar ao banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: criar banco de dados do sistema<br />
(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</p></td>
<td><p>Indica se um banco de dados do sistema deve ser criado ao criar uma nova fonte de dados.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: modo de bloqueio de banco de dados<br />
(DBPROP_JETOLEDB_DATABASELOCKMODE)</p></td>
<td><p>Indica o modo de bloqueio desse banco de dados. O primeiro usuário que abrir o banco de dados determinará o modo utilizado enquanto ele estiver aberto.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Database Password<br />
(DBPROP_JETOLEDB_DATABASEPASSWORD)</p></td>
<td><p>Indica a senha do banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Don't Copy Locale on Compact<br />
(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</p></td>
<td><p>Indica se o Jet deve copiar informações de localidade ao compactar um banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Encrypt Database<br />
(DBPROP_JETOLEDB_ENCRYPTDATABASE)</p></td>
<td><p>Indica se um banco de dados compactado deve ser criptografado. Se esta propriedade não for definida, o banco de dados compactado será criptografado caso o banco de dados original também tenha sido criptografado.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Engine Type<br />
(DBPROP_JETOLEDB_ENGINE)</p></td>
<td><p>Indica o mecanismo de armazenamento utilizado para acessar o repositório de dados atual.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Exclusive Async Delay<br />
(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</p></td>
<td><p>Indica o maior intervalo de tempo, em milissegundos, durante o qual o Jet poderá retardar as gravações assíncronas em disco quando o banco de dados estiver aberto exclusivamente. Esta propriedade será ignorada, a menos que <strong>Jet OLEDB:Flush Transaction Timeout</strong> tenha sido definida como 0.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Flush Transaction Timeout<br />
(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</p></td>
<td><p>Indica o intervalo de espera antes que os dados armazenados em um cache para gravação assíncrona sejam efetivamente gravados em disco. Essa configuração substitui os valores de <strong>Jet OLEDB:Shared Async Delay</strong> e <strong>Jet OLEDB:Exclusive Async Delay</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: transações globais em massa<br />
(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</p></td>
<td><p>Indica se transações SQL em massa serão transacionadas.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: operações em massa parciais globais<br />
(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</p></td>
<td><p>Indica a senha utilizada para abrir o banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Implicit Commit Sync<br />
(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</p></td>
<td><p>Indica se as alterações feitas em transações implícitas internas serão gravadas em modo síncrono ou assíncrono.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Lock Delay<br />
(DBPROP_JETOLEDB_LOCKDELAY)</p></td>
<td><p>Indica o número de milissegundos de espera para tentar adquirir um bloqueio depois que uma tentativa anterior falhar.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Lock Retry<br />
(DBPROP_JETOLEDB_LOCKRETRY)</p></td>
<td><p>Indica quantas vezes será repetida uma tentativa de acessar uma página bloqueada.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Max Buffer Size<br />
(DBPROP_JETOLEDB_MAXBUFFERSIZE)</p></td>
<td><p>Indica a quantidade máxima de memória, em quilobytes, que o Jet pode utilizar antes de começar a liberar as alterações para o disco.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Max Locks Per File<br />
(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</p></td>
<td><p>Indica o número máximo de bloqueios que o Jet pode colocar em um banco de dados. O valor padrão é 9500.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: nova senha de banco de dados<br />
(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</p></td>
<td><p>Indica a nova senha a ser definida para esse banco de dados. A senha anterior é armazenada em <strong>Jet OLEDB:Database Password</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: tempo limite do comando ODBC<br />
(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</p></td>
<td><p>Indica o número de milissegundos antes que uma consulta ODBC remota do Jet atinja o tempo limite.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: bloqueios de página para bloqueio de tabela<br />
(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</p></td>
<td><p>Indica quantas páginas devem ser bloqueadas dentro de uma transação antes que o Jet tente promover o bloqueio para um bloqueio de tabela. Se o valor for 0, o bloqueio nunca será promovido.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Page Timeout<br />
(DBPROP_JETOLEDB_PAGETIMEOUT)</p></td>
<td><p>Indica quantos milissegundos o Jet esperará antes de verificar se seu cache está desatualizado em relação ao arquivo do banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Recycle Long-Valued Pages<br />
(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</p></td>
<td><p>Indica se o Jet deve tentar recuperar páginas BLOB agressivamente quando estas forem liberadas.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Registry Path<br />
(DBPROP_JETOLEDB_REGPATH)</p></td>
<td><p>Indica a chave de registro do Windows que contém valores para o mecanismo de banco de dados do Jet.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: redefinir estatísticas de ISAM<br />
(DBPROP_JETOLEDB_RESETISAMSTATS)</p></td>
<td><p>Indica se o esquema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS deve redefinir seus contadores de desempenho depois de retornar informações sobre desempenho.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Shared Async Delay<br />
(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</p></td>
<td><p>Indica o maior intervalo de tempo, em milissegundos, durante o qual o Jet poderá retardar as gravações assíncronas em disco quando o banco de dados estiver aberto em modo multiusuário.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:System Database<br />
(DBPROP_JETOLEDB_SYSDBPATH)</p></td>
<td><p>Indica o caminho e o nome do arquivo de informações do grupo de trabalho (banco de dados do sistema).</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: modo de confirmação de transação<br />
(DBPROP_JETOLEDB_TXNCOMMITMODE)</p></td>
<td><p>Indica se o Jet deverá gravar dados em disco em modo síncrono ou assíncrono quando uma transação for confirmada.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:User Commit Sync<br />
(DBPROP_JETOLEDB_USERCOMMITSYNC)</p></td>
<td><p>Indica se as alterações feitas em transações serão gravadas em modo síncrono ou assíncrono.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Propriedades de Recordset e Command específicas para provedor

O provedor Jet também oferece suporte a várias propriedades **Recordset** e **Command** específicas para provedor. Essas propriedades são acessadas e definidas por meio da coleção **Properties** do objeto **Recordset** ou **Command**. A tabela lista o nome da propriedade do ADO e, entre parênteses, o nome da propriedade do OLE DB correspondente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da Propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Jet OLEDB: transações em massa<br />
(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</p></td>
<td><p>Indica se operações SQL em massa serão transacionadas. Grandes operações em massa podem falhar quando transacionadas devido aos atrasos de recursos.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: habilitar cursores de Fat<br />
(DBPROP_JETOLEDB_ENABLEFATCURSOR)</p></td>
<td><p>Indica se o Jet deve armazenar várias linhas em cache ao preencher um conjunto de registros usando fontes remotas de linhas.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: tamanho do cache de cursor fat<br />
(DBPROP_JETOLEDB_FATCURSORMAXROWS)</p></td>
<td><p>Indica o número de linhas que serão armazenadas em cache quando o cache de linhas do repositório de dados remoto estiver sendo utilizado. Este valor será ignorado, a menos que <strong>Jet OLEDB:Enable Fat Cursors</strong> seja True.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: inconsistente<br />
(DBPROP_JETOLEDB_INCONSISTENT)</p></td>
<td><p>Indica se os resultados de consultas permitem atualizações inconsistentes.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: granularidade de bloqueio<br />
(DBPROP_JETOLEDB_LOCKGRANULARITY)</p></td>
<td><p>Indica se uma tabela é aberta usando bloqueio no nível de linha.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: instrução de passagem ODBC<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</p></td>
<td><p>Indica que o Jet deve passar o texto SQL de um objeto <strong>Command</strong> inalterado para o back-end.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: operações em massa parciais<br />
(DBPROP_JETOLEDB_BULKPARTIAL)</p></td>
<td><p>Indica o comportamento do Jet quando operações SQL DML falharem.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: passagem de consulta de cooperação<br />
(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</p></td>
<td><p>Indica se as consultas que não retornam um <strong>Recordset</strong> são passadas inalteradas para a fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: passagem de cadeia de caracteres de conexão de consulta<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</p></td>
<td><p>Indica a sequência de conexão do Jet utilizada para estabelecer a conexão com um repositório remoto de dados. Este valor será ignorado, a menos que <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> seja True.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: consulta armazenada<br />
(DBPROP_JETOLEDB_STOREDQUERY)</p></td>
<td><p>Indica se o texto de comando deve ser interpretado como uma consulta armazenada em vez de um comando SQL.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: validar regras no conjunto<br />
(DBPROP_JETOLEDB_VALIDATEONSET)</p></td>
<td><p>Indica se as regras de validação do Jet serão avaliadas quando os dados das colunas forem definidos ou quando as alterações forem confirmadas no banco de dados.</p></td>
</tr>
</tbody>
</table>


Por padrão, o OLE DB Provider for Microsoft Jet abre bancos de dados do Microsoft Jet em modo de leitura/gravação. Para abrir um banco de dados em modo somente leitura, defina a propriedade [Mode](mode-property-ado.md) do objeto **Connection** do ADO como **adModeRead**.

## <a name="command-object-usage"></a>Uso do objeto Command

O texto de comando do objeto [Command](command-object-ado.md) usa o dialeto Microsoft Jet SQL. Você pode especificar consultas que retornem linhas, consultas ação e nomes de tabelas no texto de comando; entretanto, não há suporte para  procedimentos armazenados, que não devem ser especificados.

## <a name="recordset-behavior"></a>Comportamento do Recordset

O mecanismo de banco de dados do Microsoft Jet não oferece suporte a cursores dinâmicos. Portanto, o OLE DB Provider for Microsoft Jet não oferece suporte ao tipo de cursor **adLockDynamic**. Quando um cursor dinâmico é solicitado, o provedor retorna um cursor de conjunto de chaves e redefine a propriedade [CursorType](cursortype-property-ado.md) para indicar o tipo de [Recordset](recordset-object-ado.md) retornado. Além disso, quando um **Recordset** que pode ser atualizado é solicitado (**LockType** é **adLockOptimistic**, **adLockBatchOptimistic** ou **adLockPessimistic**), o provedor também retorna um cursor de conjunto de chaves e redefine a propriedade **CursorType**.

## <a name="dynamic-properties"></a>Propriedades dinâmicas

O OLE DB Provider for Microsoft Jet insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.

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
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="odd">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="even">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
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
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="even">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="odd">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
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
<td><p>Modo</p></td>
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
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="even">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Senha</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
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
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarks Ordered</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Cache Deferred Columns</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Column Writable</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Defer Column</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="odd">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="even">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="even">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="odd">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="even">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="odd">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsestLocate</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Essa</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
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
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="even">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
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
<td><p>Memory Usage</p></td>
<td><p>DBPROP_MEMORYUSAGE</p></td>
</tr>
<tr class="even">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Others' Changes Visible</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Others' Inserts Visible</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Atualização</p></td>
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
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="even">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Defer Column</p></td>
<td><p>DBPROP_DEFERRED</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
</tr>
<tr class="odd">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
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
<td><p>Essa</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="even">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="odd">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="even">
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
</tr>
<tr class="even">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="odd">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Lock Mode</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
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
<td><p>Others' Changes Visible</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Others' Inserts Visible</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
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
<td><p>Server Data on Insert</p></td>
<td><p>DBPROP_SERVERDATAONINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="even">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Atualização</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

Para obter detalhes específicos sobre a implementação e informações funcionais sobre o OLE DB Provider for Microsoft Jet, consulte a documentação do OLE DB Provider for Microsoft Jet no MDAC SDK.

