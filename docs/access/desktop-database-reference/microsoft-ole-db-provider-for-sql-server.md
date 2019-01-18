---
title: Microsoft OLE DB Provider for SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705103"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="66d6a-102">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="66d6a-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="66d6a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="66d6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66d6a-104">O Microsoft OLE DB Provider for SQL Server, SQLOLEDB, permite que o ADO acesse o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66d6a-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="66d6a-105">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="66d6a-105">Connection String Parameters</span></span>

<span data-ttu-id="66d6a-106">Para se conectar com esse provedor, defina o argumento *Provider* para a propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="66d6a-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="66d6a-107">Esse valor também pode ser definido ou lido usando a propriedade [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="66d6a-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="66d6a-108">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="66d6a-108">Typical Connection String</span></span>

<span data-ttu-id="66d6a-109">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="66d6a-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="66d6a-110">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="66d6a-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66d6a-111">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="66d6a-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="66d6a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="66d6a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="66d6a-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="66d6a-114">Especifica o Microsoft OLE DB Provider for SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66d6a-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-115"><strong>Data Source</strong> ou <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="66d6a-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="66d6a-116">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="66d6a-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-117"><strong>Initial Catalog</strong> ou <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="66d6a-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="66d6a-118">Especifica o nome de um banco de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="66d6a-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-119"><strong>User ID</strong> ou <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="66d6a-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="66d6a-120">Especifica o nome do usuário (para autenticação no SQL Server).</span><span class="sxs-lookup"><span data-stu-id="66d6a-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-121"><strong>Password</strong> ou <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="66d6a-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="66d6a-122">Especifica a senha do usuário (para autenticação no SQL Server).</span><span class="sxs-lookup"><span data-stu-id="66d6a-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="66d6a-123">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="66d6a-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="66d6a-p101">O provedor oferece suporte a vários parâmetros de conexão específicos para provedor, além daqueles definidos pelo ADO. Assim como as propriedades de conexão do ADO, essas propriedades específicas para provedor podem ser definidas pela coleção [Properties](properties-collection-ado.md) de um objeto [Connection](connection-object-ado.md) ou como parte da **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66d6a-126">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="66d6a-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="66d6a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="66d6a-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="66d6a-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="66d6a-p102">Indica o modo de autenticação do usuário. Pode ser definido como <strong>Yes</strong> ou <strong>No</strong>. O valor padrão é <strong>No</strong>. Se esta propriedade for definida como <strong>Yes</strong>, o SQLOLEDB usará o Modo de Autenticação do Microsoft Windows NT para autorizar o acesso do usuário ao banco de dados do SQL Server especificado pelos valores das propriedades <strong>Location</strong> e <a href="datasource-property-ado.md">Datasource</a>. Se esta propriedade for definida como <strong>No</strong>, o SQLOLEDB usará o Modo Misto para autorizar o acesso do usuário ao banco de dados do SQL Server. O logon e senha para acesso ao SQL Server são especificados nas propriedades <strong>User Id</strong> e <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="66d6a-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="66d6a-p103">Indica o nome de um idioma no SQL Server. Identifica o idioma utilizado para a seleção e formatação de mensagens do sistema. Se esse idioma não estiver instalado no SQL Server, ocorrerá falha na abertura da conexão.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="66d6a-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="66d6a-140">Indica o endereço de rede do SQL Server especificado pela propriedade <strong>Location</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d6a-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="66d6a-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="66d6a-142">Indica o nome da biblioteca de rede (bibliotecas de vínculos dinâmicos) usado para se comunicar com o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66d6a-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="66d6a-143">O nome não deve incluir o caminho ou a extensão de nome de arquivo. dll.</span><span class="sxs-lookup"><span data-stu-id="66d6a-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="66d6a-144">O padrão é fornecido pela configuração de cliente do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66d6a-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="66d6a-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="66d6a-146">Determina se o SQL Server cria procedimentos armazenados temporários quando Commands são preparados (pela propriedade <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="66d6a-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="66d6a-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="66d6a-p105">Indica se os caracteres OEM/ANSI serão convertidos. Esta propriedade pode ser definida como <strong>True</strong> ou <strong>False</strong>. O valor padrão é <strong>True</strong>. Se esta propriedade for definida como <strong>True</strong>, o SQLOLEDB realizará a conversão de caracteres OEM/ANSI sempre que cadeias de caracteres de bytes múltiplos forem recuperadas no SQL Server ou enviadas para ele. Se for definida como <strong>False</strong>, o SQLOLEDB não realizará a conversão de caracteres OEM/ANSI em dados de cadeias de caracteres de bytes múltiplos.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="66d6a-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="66d6a-p106">Indica o tamanho de um pacote de rede em bytes. O valor desta propriedade deverá estar entre 512 e 32767. O tamanho padrão do pacote de rede SQLOLEDB é 4096.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-158">Indica o nome do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="66d6a-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="66d6a-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="66d6a-160">Uma cadeia de caracteres identificando a estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="66d6a-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="66d6a-161">Uso do objeto Command</span><span class="sxs-lookup"><span data-stu-id="66d6a-161">Command Object Usage</span></span>

<span data-ttu-id="66d6a-p107">O SQLOLEDB aceita uma combinação de ODBC, ANSI e Transact-SQL específico do SQL Server como sintaxe válida. Por exemplo, esta instrução SQL utiliza uma sequência de escape ODBC SQL para especificar a função de cadeia de caracteres LCASE:</span><span class="sxs-lookup"><span data-stu-id="66d6a-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="66d6a-p108">LCASE retorna uma cadeia de caracteres, convertendo todos os caracteres maiúsculos para seus equivalentes minúsculos. A função da sequência ANSI SQL LOWER executa a mesma operação, sendo assim, esta instrução SQL é um equivalente ANSI da instrução ODBC acima:</span><span class="sxs-lookup"><span data-stu-id="66d6a-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="66d6a-166">O SQLOLEDB processará com sucesso ambas as formas desta instrução, quando especificadas como texto para um comando.</span><span class="sxs-lookup"><span data-stu-id="66d6a-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="66d6a-167">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="66d6a-167">Stored Procedures</span></span>

<span data-ttu-id="66d6a-p109">Ao executar um procedimento armazenado do SQL Server utilizando um comando SQLOLEDB, use a sequência de escape de chamada de procedimento ODBC no texto de comando. Assim, o SQLOLEDB usará o mecanismo de chamada de procedimento remoto do SQL Server para otimizar o processamento do comando. Por exemplo, esta instrução ODBC SQL no texto de comando é preferível ao Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="66d6a-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="66d6a-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="66d6a-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="66d6a-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="66d6a-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="66d6a-173">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="66d6a-173">Recordset Behavior</span></span>

<span data-ttu-id="66d6a-p110">O SQLOLEDB não pode usar cursores do SQL Server para oferecer suporte aos múltiplos resultados gerados por vários comandos. Se um consumidor solicitar um conjunto de registros que exija suporte a cursores do SQL Server, ocorrerá um erro caso o texto de comando utilizado gere mais que um único conjunto de registros como resultado.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="66d6a-p111">Os cursores do SQL Server oferecem suporte a conjuntos de registros roláveis do SQLOLEDB. O SQL Server impõe certas limitações a cursores que sejam sensíveis a alterações feitas por outros usuários do banco de dados. Especificamente, as linhas em alguns cursores não podem ser classificadas, e qualquer tentativa de criar um conjunto de registros usando um comando que contenha uma cláusula SQL ORDER BY poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="66d6a-179">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="66d6a-179">Dynamic Properties</span></span>

<span data-ttu-id="66d6a-180">O Microsoft OLE DB Provider for SQL Server insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="66d6a-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="66d6a-p112">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="66d6a-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="66d6a-185">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="66d6a-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="66d6a-186">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="66d6a-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66d6a-187">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="66d6a-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="66d6a-188">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="66d6a-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="66d6a-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="66d6a-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="66d6a-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="66d6a-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="66d6a-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="66d6a-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="66d6a-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="66d6a-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="66d6a-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="66d6a-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="66d6a-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="66d6a-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="66d6a-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="66d6a-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="66d6a-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="66d6a-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="66d6a-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="66d6a-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="66d6a-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="66d6a-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="66d6a-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="66d6a-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="66d6a-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="66d6a-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="66d6a-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="66d6a-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="66d6a-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="66d6a-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="66d6a-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="66d6a-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="66d6a-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="66d6a-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="66d6a-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="66d6a-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="66d6a-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="66d6a-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="66d6a-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="66d6a-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="66d6a-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="66d6a-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="66d6a-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="66d6a-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="66d6a-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="66d6a-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="66d6a-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="66d6a-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="66d6a-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="66d6a-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="66d6a-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="66d6a-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="66d6a-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="66d6a-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="66d6a-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="66d6a-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="66d6a-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="66d6a-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="66d6a-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="66d6a-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="66d6a-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="66d6a-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="66d6a-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="66d6a-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="66d6a-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="66d6a-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="66d6a-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="66d6a-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="66d6a-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="66d6a-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="66d6a-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="66d6a-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="66d6a-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="66d6a-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="66d6a-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="66d6a-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="66d6a-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="66d6a-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="66d6a-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="66d6a-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="66d6a-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="66d6a-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="66d6a-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="66d6a-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="66d6a-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="66d6a-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="66d6a-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="66d6a-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="66d6a-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="66d6a-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="66d6a-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="66d6a-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="66d6a-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="66d6a-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="66d6a-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="66d6a-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="66d6a-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="66d6a-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="66d6a-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-265">Password</span><span class="sxs-lookup"><span data-stu-id="66d6a-265">Password</span></span></p></td>
<td><p><span data-ttu-id="66d6a-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="66d6a-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="66d6a-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="66d6a-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="66d6a-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="66d6a-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="66d6a-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="66d6a-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="66d6a-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="66d6a-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="66d6a-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="66d6a-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="66d6a-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="66d6a-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="66d6a-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="66d6a-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="66d6a-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="66d6a-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="66d6a-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="66d6a-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="66d6a-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="66d6a-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="66d6a-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="66d6a-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="66d6a-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="66d6a-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="66d6a-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="66d6a-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="66d6a-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="66d6a-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="66d6a-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="66d6a-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="66d6a-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="66d6a-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="66d6a-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="66d6a-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="66d6a-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="66d6a-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="66d6a-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="66d6a-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="66d6a-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="66d6a-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="66d6a-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="66d6a-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="66d6a-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="66d6a-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="66d6a-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="66d6a-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-303">User ID</span><span class="sxs-lookup"><span data-stu-id="66d6a-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="66d6a-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="66d6a-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-305">User Name</span><span class="sxs-lookup"><span data-stu-id="66d6a-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="66d6a-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="66d6a-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="66d6a-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="66d6a-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="66d6a-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="66d6a-309">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="66d6a-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="66d6a-310">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="66d6a-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66d6a-311">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="66d6a-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="66d6a-312">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="66d6a-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="66d6a-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="66d6a-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="66d6a-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="66d6a-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="66d6a-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="66d6a-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="66d6a-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="66d6a-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="66d6a-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="66d6a-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="66d6a-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="66d6a-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="66d6a-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="66d6a-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="66d6a-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="66d6a-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="66d6a-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="66d6a-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="66d6a-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="66d6a-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="66d6a-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="66d6a-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="66d6a-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="66d6a-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="66d6a-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="66d6a-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="66d6a-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="66d6a-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="66d6a-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="66d6a-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="66d6a-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="66d6a-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="66d6a-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="66d6a-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="66d6a-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="66d6a-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="66d6a-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="66d6a-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="66d6a-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="66d6a-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="66d6a-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="66d6a-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="66d6a-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="66d6a-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="66d6a-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="66d6a-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="66d6a-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="66d6a-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="66d6a-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="66d6a-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="66d6a-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="66d6a-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="66d6a-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="66d6a-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="66d6a-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="66d6a-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="66d6a-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="66d6a-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="66d6a-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="66d6a-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="66d6a-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="66d6a-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="66d6a-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="66d6a-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="66d6a-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="66d6a-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="66d6a-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="66d6a-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="66d6a-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="66d6a-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="66d6a-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="66d6a-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="66d6a-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="66d6a-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="66d6a-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="66d6a-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="66d6a-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="66d6a-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="66d6a-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="66d6a-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="66d6a-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="66d6a-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="66d6a-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="66d6a-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="66d6a-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="66d6a-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="66d6a-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="66d6a-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="66d6a-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="66d6a-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="66d6a-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="66d6a-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="66d6a-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="66d6a-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="66d6a-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="66d6a-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="66d6a-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="66d6a-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="66d6a-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="66d6a-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="66d6a-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="66d6a-444">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="66d6a-444">Command Dynamic Properties</span></span>

<span data-ttu-id="66d6a-445">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="66d6a-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66d6a-446">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="66d6a-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="66d6a-447">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="66d6a-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="66d6a-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="66d6a-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="66d6a-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="66d6a-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="66d6a-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="66d6a-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="66d6a-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="66d6a-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="66d6a-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="66d6a-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="66d6a-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="66d6a-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="66d6a-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="66d6a-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="66d6a-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="66d6a-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="66d6a-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="66d6a-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="66d6a-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="66d6a-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="66d6a-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="66d6a-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="66d6a-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="66d6a-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="66d6a-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="66d6a-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="66d6a-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="66d6a-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="66d6a-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="66d6a-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="66d6a-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="66d6a-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="66d6a-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="66d6a-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="66d6a-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="66d6a-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="66d6a-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="66d6a-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="66d6a-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="66d6a-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="66d6a-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="66d6a-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="66d6a-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="66d6a-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="66d6a-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="66d6a-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="66d6a-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="66d6a-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="66d6a-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="66d6a-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="66d6a-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="66d6a-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="66d6a-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="66d6a-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="66d6a-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="66d6a-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="66d6a-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="66d6a-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="66d6a-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="66d6a-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="66d6a-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="66d6a-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="66d6a-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="66d6a-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="66d6a-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="66d6a-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="66d6a-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="66d6a-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="66d6a-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="66d6a-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="66d6a-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="66d6a-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="66d6a-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="66d6a-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="66d6a-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="66d6a-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="66d6a-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="66d6a-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="66d6a-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="66d6a-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="66d6a-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="66d6a-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="66d6a-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="66d6a-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="66d6a-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="66d6a-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="66d6a-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="66d6a-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="66d6a-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="66d6a-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="66d6a-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="66d6a-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="66d6a-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="66d6a-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="66d6a-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="66d6a-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="66d6a-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="66d6a-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="66d6a-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="66d6a-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="66d6a-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="66d6a-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="66d6a-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="66d6a-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="66d6a-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="66d6a-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="66d6a-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="66d6a-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="66d6a-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="66d6a-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="66d6a-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="66d6a-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="66d6a-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="66d6a-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="66d6a-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="66d6a-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="66d6a-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="66d6a-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="66d6a-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="66d6a-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="66d6a-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="66d6a-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="66d6a-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="66d6a-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="66d6a-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="66d6a-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="66d6a-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="66d6a-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="66d6a-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="66d6a-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="66d6a-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="66d6a-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="66d6a-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="66d6a-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="66d6a-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="66d6a-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="66d6a-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="66d6a-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="66d6a-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="66d6a-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="66d6a-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66d6a-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="66d6a-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="66d6a-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="66d6a-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66d6a-594">XSL</span><span class="sxs-lookup"><span data-stu-id="66d6a-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="66d6a-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="66d6a-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66d6a-596">Para obter detalhes específicos sobre a implementação e informações funcionais sobre o Microsoft OLE DB Provider for SQL Server, consulte a documentação do OLE DB Provider for SQL Server na seção OLE DB do MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="66d6a-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

