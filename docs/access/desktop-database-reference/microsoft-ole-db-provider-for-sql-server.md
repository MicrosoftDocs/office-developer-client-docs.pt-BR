---
title: Microsoft OLE DB Provider for SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c856b2ba8d39c9cfc03bdadd6250ee9411b9c9c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883887"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="1f542-102">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="1f542-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="1f542-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f542-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f542-104">O Microsoft OLE DB Provider for SQL Server, SQLOLEDB, permite que o ADO acesse o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f542-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="1f542-105">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="1f542-105">Connection String Parameters</span></span>

<span data-ttu-id="1f542-106">Para se conectar com esse provedor, defina o argumento *Provider* para a propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="1f542-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="1f542-107">Esse valor também pode ser definido ou lido usando a propriedade [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1f542-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="1f542-108">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="1f542-108">Typical Connection String</span></span>

<span data-ttu-id="1f542-109">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="1f542-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="1f542-110">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="1f542-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f542-111">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="1f542-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="1f542-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f542-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f542-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="1f542-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="1f542-114">Especifica o Microsoft OLE DB Provider for SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f542-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-115"><strong>Data Source</strong> ou <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1f542-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1f542-116">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1f542-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-117"><strong>Initial Catalog</strong> ou <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="1f542-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="1f542-118">Especifica o nome de um banco de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="1f542-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-119"><strong>User ID</strong> ou <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="1f542-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="1f542-120">Especifica o nome do usuário (para autenticação no SQL Server).</span><span class="sxs-lookup"><span data-stu-id="1f542-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-121"><strong>Password</strong> ou <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="1f542-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="1f542-122">Especifica a senha do usuário (para autenticação no SQL Server).</span><span class="sxs-lookup"><span data-stu-id="1f542-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="1f542-123">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="1f542-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="1f542-p101">O provedor oferece suporte a vários parâmetros de conexão específicos para provedor, além daqueles definidos pelo ADO. Assim como as propriedades de conexão do ADO, essas propriedades específicas para provedor podem ser definidas pela coleção [Properties](properties-collection-ado.md) de um objeto [Connection](connection-object-ado.md) ou como parte da **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="1f542-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f542-126">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f542-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1f542-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f542-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f542-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="1f542-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="1f542-p102">Indica o modo de autenticação do usuário. Pode ser definido como <strong>Yes</strong> ou <strong>No</strong>. O valor padrão é <strong>No</strong>. Se esta propriedade for definida como <strong>Yes</strong>, o SQLOLEDB usará o Modo de Autenticação do Microsoft Windows NT para autorizar o acesso do usuário ao banco de dados do SQL Server especificado pelos valores das propriedades <strong>Location</strong> e <a href="datasource-property-ado.md">Datasource</a>. Se esta propriedade for definida como <strong>No</strong>, o SQLOLEDB usará o Modo Misto para autorizar o acesso do usuário ao banco de dados do SQL Server. O logon e senha para acesso ao SQL Server são especificados nas propriedades <strong>User Id</strong> e <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f542-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="1f542-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="1f542-p103">Indica o nome de um idioma no SQL Server. Identifica o idioma utilizado para a seleção e formatação de mensagens do sistema. Se esse idioma não estiver instalado no SQL Server, ocorrerá falha na abertura da conexão.</span><span class="sxs-lookup"><span data-stu-id="1f542-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="1f542-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="1f542-140">Indica o endereço de rede do SQL Server especificado pela propriedade <strong>Location</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f542-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="1f542-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="1f542-142">Indica o nome da biblioteca de rede (bibliotecas de vínculos dinâmicos) usado para se comunicar com o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f542-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="1f542-143">O nome não deve incluir o caminho ou a extensão de nome de arquivo. dll.</span><span class="sxs-lookup"><span data-stu-id="1f542-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="1f542-144">O padrão é fornecido pela configuração de cliente do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f542-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="1f542-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="1f542-146">Determina se o SQL Server cria procedimentos armazenados temporários quando Commands são preparados (pela propriedade <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="1f542-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="1f542-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="1f542-p105">Indica se os caracteres OEM/ANSI serão convertidos. Esta propriedade pode ser definida como <strong>True</strong> ou <strong>False</strong>. O valor padrão é <strong>True</strong>. Se esta propriedade for definida como <strong>True</strong>, o SQLOLEDB realizará a conversão de caracteres OEM/ANSI sempre que cadeias de caracteres de bytes múltiplos forem recuperadas no SQL Server ou enviadas para ele. Se for definida como <strong>False</strong>, o SQLOLEDB não realizará a conversão de caracteres OEM/ANSI em dados de cadeias de caracteres de bytes múltiplos.</span><span class="sxs-lookup"><span data-stu-id="1f542-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="1f542-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="1f542-p106">Indica o tamanho de um pacote de rede em bytes. O valor desta propriedade deverá estar entre 512 e 32767. O tamanho padrão do pacote de rede SQLOLEDB é 4096.</span><span class="sxs-lookup"><span data-stu-id="1f542-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="1f542-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-158">Indica o nome do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1f542-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="1f542-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="1f542-160">Uma cadeia de caracteres identificando a estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1f542-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="1f542-161">Uso do objeto Command</span><span class="sxs-lookup"><span data-stu-id="1f542-161">Command Object Usage</span></span>

<span data-ttu-id="1f542-p107">O SQLOLEDB aceita uma combinação de ODBC, ANSI e Transact-SQL específico do SQL Server como sintaxe válida. Por exemplo, esta instrução SQL utiliza uma sequência de escape ODBC SQL para especificar a função de cadeia de caracteres LCASE:</span><span class="sxs-lookup"><span data-stu-id="1f542-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="1f542-p108">LCASE retorna uma cadeia de caracteres, convertendo todos os caracteres maiúsculos para seus equivalentes minúsculos. A função da sequência ANSI SQL LOWER executa a mesma operação, sendo assim, esta instrução SQL é um equivalente ANSI da instrução ODBC acima:</span><span class="sxs-lookup"><span data-stu-id="1f542-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="1f542-166">O SQLOLEDB processará com sucesso ambas as formas desta instrução, quando especificadas como texto para um comando.</span><span class="sxs-lookup"><span data-stu-id="1f542-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="1f542-167">Procedimentos armazenados</span><span class="sxs-lookup"><span data-stu-id="1f542-167">Stored Procedures</span></span>

<span data-ttu-id="1f542-p109">Ao executar um procedimento armazenado do SQL Server utilizando um comando SQLOLEDB, use a sequência de escape de chamada de procedimento ODBC no texto de comando. Assim, o SQLOLEDB usará o mecanismo de chamada de procedimento remoto do SQL Server para otimizar o processamento do comando. Por exemplo, esta instrução ODBC SQL no texto de comando é preferível ao Transact-SQL:</span><span class="sxs-lookup"><span data-stu-id="1f542-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="1f542-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="1f542-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="1f542-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="1f542-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="1f542-173">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="1f542-173">Recordset Behavior</span></span>

<span data-ttu-id="1f542-p110">O SQLOLEDB não pode usar cursores do SQL Server para oferecer suporte aos múltiplos resultados gerados por vários comandos. Se um consumidor solicitar um conjunto de registros que exija suporte a cursores do SQL Server, ocorrerá um erro caso o texto de comando utilizado gere mais que um único conjunto de registros como resultado.</span><span class="sxs-lookup"><span data-stu-id="1f542-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="1f542-p111">Os cursores do SQL Server oferecem suporte a conjuntos de registros roláveis do SQLOLEDB. O SQL Server impõe certas limitações a cursores que sejam sensíveis a alterações feitas por outros usuários do banco de dados. Especificamente, as linhas em alguns cursores não podem ser classificadas, e qualquer tentativa de criar um conjunto de registros usando um comando que contenha uma cláusula SQL ORDER BY poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="1f542-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="1f542-179">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="1f542-179">Dynamic Properties</span></span>

<span data-ttu-id="1f542-180">O Microsoft OLE DB Provider for SQL Server insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="1f542-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="1f542-p112">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1f542-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="1f542-185">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="1f542-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="1f542-186">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="1f542-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f542-187">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="1f542-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f542-188">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f542-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f542-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="1f542-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="1f542-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="1f542-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="1f542-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="1f542-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="1f542-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="1f542-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="1f542-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="1f542-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f542-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f542-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f542-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="1f542-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="1f542-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="1f542-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="1f542-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="1f542-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="1f542-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="1f542-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="1f542-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="1f542-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="1f542-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="1f542-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1f542-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="1f542-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="1f542-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="1f542-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="1f542-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f542-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="1f542-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="1f542-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="1f542-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f542-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f542-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f542-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="1f542-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="1f542-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="1f542-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="1f542-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="1f542-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="1f542-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="1f542-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="1f542-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="1f542-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="1f542-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="1f542-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="1f542-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="1f542-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="1f542-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="1f542-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="1f542-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="1f542-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f542-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="1f542-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="1f542-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="1f542-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="1f542-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="1f542-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="1f542-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="1f542-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="1f542-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="1f542-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="1f542-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="1f542-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="1f542-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="1f542-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="1f542-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="1f542-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="1f542-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="1f542-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="1f542-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="1f542-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="1f542-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f542-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="1f542-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="1f542-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="1f542-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="1f542-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="1f542-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="1f542-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f542-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f542-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="1f542-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="1f542-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f542-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="1f542-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="1f542-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="1f542-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="1f542-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f542-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f542-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="1f542-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="1f542-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="1f542-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="1f542-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="1f542-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f542-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="1f542-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="1f542-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="1f542-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="1f542-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="1f542-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="1f542-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="1f542-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="1f542-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="1f542-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-265">Password</span><span class="sxs-lookup"><span data-stu-id="1f542-265">Password</span></span></p></td>
<td><p><span data-ttu-id="1f542-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="1f542-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="1f542-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="1f542-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="1f542-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="1f542-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="1f542-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="1f542-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="1f542-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f542-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f542-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="1f542-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="1f542-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="1f542-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="1f542-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="1f542-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="1f542-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="1f542-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="1f542-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="1f542-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="1f542-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="1f542-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="1f542-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="1f542-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="1f542-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="1f542-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="1f542-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="1f542-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="1f542-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="1f542-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="1f542-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="1f542-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="1f542-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="1f542-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="1f542-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="1f542-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="1f542-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="1f542-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f542-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="1f542-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f542-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="1f542-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="1f542-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="1f542-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="1f542-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="1f542-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="1f542-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="1f542-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="1f542-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="1f542-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="1f542-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="1f542-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="1f542-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-303">User ID</span><span class="sxs-lookup"><span data-stu-id="1f542-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="1f542-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="1f542-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-305">User Name</span><span class="sxs-lookup"><span data-stu-id="1f542-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="1f542-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="1f542-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="1f542-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="1f542-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="1f542-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="1f542-309">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="1f542-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="1f542-310">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1f542-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f542-311">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="1f542-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f542-312">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f542-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f542-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f542-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f542-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f542-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f542-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f542-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f542-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f542-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f542-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f542-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f542-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f542-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f542-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f542-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f542-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f542-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="1f542-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="1f542-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1f542-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f542-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f542-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f542-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f542-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f542-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f542-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f542-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f542-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f542-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f542-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f542-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f542-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f542-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f542-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f542-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f542-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f542-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f542-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f542-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f542-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f542-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f542-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f542-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f542-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f542-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f542-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f542-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="1f542-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f542-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f542-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f542-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f542-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f542-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f542-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f542-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f542-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f542-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f542-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f542-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f542-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f542-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f542-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f542-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f542-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f542-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f542-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f542-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f542-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f542-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f542-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f542-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f542-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f542-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f542-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f542-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f542-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f542-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f542-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f542-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f542-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f542-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f542-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f542-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f542-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f542-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f542-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f542-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f542-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f542-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f542-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f542-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f542-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f542-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f542-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f542-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f542-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f542-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f542-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f542-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f542-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f542-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f542-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="1f542-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="1f542-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="1f542-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="1f542-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f542-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f542-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f542-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f542-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f542-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f542-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f542-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="1f542-444">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="1f542-444">Command Dynamic Properties</span></span>

<span data-ttu-id="1f542-445">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="1f542-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f542-446">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="1f542-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="1f542-447">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="1f542-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f542-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="1f542-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="1f542-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="1f542-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="1f542-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="1f542-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="1f542-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="1f542-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="1f542-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="1f542-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="1f542-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="1f542-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="1f542-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="1f542-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="1f542-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="1f542-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f542-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f542-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="1f542-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="1f542-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="1f542-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="1f542-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="1f542-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="1f542-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="1f542-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="1f542-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="1f542-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="1f542-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="1f542-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="1f542-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="1f542-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="1f542-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="1f542-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="1f542-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="1f542-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f542-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f542-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f542-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="1f542-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="1f542-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="1f542-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f542-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="1f542-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="1f542-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f542-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="1f542-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="1f542-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="1f542-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="1f542-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f542-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="1f542-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="1f542-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f542-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="1f542-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="1f542-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f542-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="1f542-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="1f542-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f542-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="1f542-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="1f542-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f542-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="1f542-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="1f542-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f542-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="1f542-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="1f542-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f542-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="1f542-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="1f542-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="1f542-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="1f542-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f542-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f542-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f542-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f542-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="1f542-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="1f542-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="1f542-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="1f542-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="1f542-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="1f542-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="1f542-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="1f542-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="1f542-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="1f542-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="1f542-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="1f542-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1f542-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="1f542-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="1f542-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="1f542-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="1f542-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="1f542-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="1f542-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="1f542-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="1f542-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="1f542-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="1f542-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f542-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="1f542-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="1f542-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="1f542-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="1f542-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="1f542-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="1f542-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="1f542-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="1f542-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="1f542-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="1f542-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="1f542-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="1f542-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="1f542-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="1f542-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="1f542-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="1f542-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="1f542-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="1f542-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="1f542-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="1f542-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="1f542-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="1f542-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="1f542-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="1f542-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="1f542-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="1f542-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="1f542-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f542-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="1f542-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="1f542-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="1f542-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="1f542-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="1f542-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="1f542-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="1f542-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="1f542-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="1f542-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="1f542-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="1f542-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="1f542-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="1f542-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="1f542-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="1f542-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="1f542-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="1f542-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="1f542-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="1f542-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="1f542-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="1f542-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="1f542-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f542-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="1f542-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="1f542-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="1f542-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f542-594">XSL</span><span class="sxs-lookup"><span data-stu-id="1f542-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="1f542-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="1f542-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f542-596">Para obter detalhes específicos sobre a implementação e informações funcionais sobre o Microsoft OLE DB Provider for SQL Server, consulte a documentação do OLE DB Provider for SQL Server na seção OLE DB do MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="1f542-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

