---
title: Microsoft OLE DB Provider for Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd56f018a9eb8da4078848d7890e4543279a7362
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462527"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="3ea6b-102">Microsoft OLE DB Provider for Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="3ea6b-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="3ea6b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ea6b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ea6b-104">O OLE DB Provider for Microsoft Jet permite que o ADO acesse bancos de dados do Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="3ea6b-105">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="3ea6b-105">Connection String Parameters</span></span>

<span data-ttu-id="3ea6b-106">Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="3ea6b-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="3ea6b-107">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="3ea6b-108">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="3ea6b-108">Typical Connection String</span></span>

<span data-ttu-id="3ea6b-109">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="3ea6b-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="3ea6b-110">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="3ea6b-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-111">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="3ea6b-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ea6b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="3ea6b-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="3ea6b-114">Especifica o OLE DB Provider for Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="3ea6b-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="3ea6b-116">Especifica o banco de dados caminho e nome de arquivo (por exemplo, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="3ea6b-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="3ea6b-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="3ea6b-118">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-118">Specifies the user name.</span></span> <span data-ttu-id="3ea6b-119">Se essa palavra-chave não for especificado, a cadeia de caracteres, &quot;admin&quot;, é usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="3ea6b-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="3ea6b-121">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-121">Specifies the user password.</span></span> <span data-ttu-id="3ea6b-122">Se essa palavra-chave não for especificado, a cadeia de caracteres vazia (&quot;&quot;), é usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="3ea6b-123">Parâmetros de conexão específicos para provedor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="3ea6b-p103">O OLE DB Provider for Microsoft Jet oferece suporte a várias propriedades dinâmicas específicas para o provedor, além daquelas definidas pelo ADO. Como ocorre com todos os demais parâmetros **Connection**, estes podem ser definidos por meio da coleção **Properties** do objeto **Connection** ou como parte da sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="3ea6b-126">A tabela abaixo relaciona essas propriedades com o nome da propriedade do OLE DB correspondente entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-127">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ea6b-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ea6b-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-129">Quantidade de espaço recuperado OLEDB:Compact Jet</span><span class="sxs-lookup"><span data-stu-id="3ea6b-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="3ea6b-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p104">Indica uma estimativa da quantidade de espaço, em bytes, que pode ser recuperada compactando-se o banco de dados. Esse valor é válido somente depois que uma conexão com o banco de dados tiver sido estabelecida.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-133">Controle de OLEDB:Connection Jet</span><span class="sxs-lookup"><span data-stu-id="3ea6b-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="3ea6b-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-135">Indica se os usuários podem se conectar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-136">Jet OLEDB: Criar banco de dados do sistema</span><span class="sxs-lookup"><span data-stu-id="3ea6b-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="3ea6b-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-138">Indica se um banco de dados do sistema deve ser criado ao criar uma nova fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-139">Modo de bloqueio de OLEDB:Database Jet</span><span class="sxs-lookup"><span data-stu-id="3ea6b-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="3ea6b-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p105">Indica o modo de bloqueio desse banco de dados. O primeiro usuário que abrir o banco de dados determinará o modo utilizado enquanto ele estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="3ea6b-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="3ea6b-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-145">Indica a senha do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="3ea6b-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="3ea6b-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-148">Indica se o Jet deve copiar informações de localidade ao compactar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="3ea6b-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="3ea6b-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p106">Indica se um banco de dados compactado deve ser criptografado. Se esta propriedade não for definida, o banco de dados compactado será criptografado caso o banco de dados original também tenha sido criptografado.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="3ea6b-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="3ea6b-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-155">Indica o mecanismo de armazenamento utilizado para acessar o repositório de dados atual.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="3ea6b-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="3ea6b-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-158">Indica o maior intervalo de tempo, em milissegundos, durante o qual o Jet poderá retardar as gravações assíncronas em disco quando o banco de dados estiver aberto exclusivamente.
</span><span class="sxs-lookup"><span data-stu-id="3ea6b-158">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</span></span> <span data-ttu-id="3ea6b-159">Esta propriedade será ignorada, a menos que <strong>Jet OLEDB:Flush Transaction Timeout</strong> tenha sido definida como 0.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-159">This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="3ea6b-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="3ea6b-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p108">Indica o intervalo de espera antes que os dados armazenados em um cache para gravação assíncrona sejam efetivamente gravados em disco. Essa configuração substitui os valores de <strong>Jet OLEDB:Shared Async Delay</strong> e <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-164">Jet OLEDB: transações em massa Global</span><span class="sxs-lookup"><span data-stu-id="3ea6b-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="3ea6b-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-166">Indica se transações SQL em massa serão transacionadas.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-167">Jet OLEDB: operações em massa de parcial Global</span><span class="sxs-lookup"><span data-stu-id="3ea6b-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="3ea6b-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-169">Indica a senha utilizada para abrir o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="3ea6b-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="3ea6b-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-172">Indica se as alterações feitas em transações implícitas internas serão gravadas em modo síncrono ou assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="3ea6b-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="3ea6b-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-175">Indica o número de milissegundos de espera para tentar adquirir um bloqueio depois que uma tentativa anterior falhar.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="3ea6b-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="3ea6b-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-178">Indica quantas vezes será repetida uma tentativa de acessar uma página bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="3ea6b-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="3ea6b-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-181">Indica a quantidade máxima de memória, em quilobytes, que o Jet pode utilizar antes de começar a liberar as alterações para o disco.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="3ea6b-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="3ea6b-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p109">Indica o número máximo de bloqueios que o Jet pode colocar em um banco de dados. O valor padrão é 9500.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-186">Jet OLEDB: nova senha de banco de dados</span><span class="sxs-lookup"><span data-stu-id="3ea6b-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="3ea6b-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p110">Indica a nova senha a ser definida para esse banco de dados. A senha anterior é armazenada em <strong>Jet OLEDB:Database Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-190">Jet OLEDB:ODBC Command Time Out</span><span class="sxs-lookup"><span data-stu-id="3ea6b-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="3ea6b-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-192">Indica o número de milissegundos antes que uma consulta ODBC remota do Jet atinja o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-193">Bloqueios do Jet OLEDB para bloqueio de tabela</span><span class="sxs-lookup"><span data-stu-id="3ea6b-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="3ea6b-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p111">Indica quantas páginas devem ser bloqueadas dentro de uma transação antes que o Jet tente promover o bloqueio para um bloqueio de tabela. Se o valor for 0, o bloqueio nunca será promovido.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="3ea6b-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="3ea6b-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-199">Indica quantos milissegundos o Jet esperará antes de verificar se seu cache está desatualizado em relação ao arquivo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="3ea6b-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="3ea6b-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-202">Indica se o Jet deve tentar recuperar páginas BLOB agressivamente quando estas forem liberadas.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="3ea6b-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="3ea6b-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-205">Indica a chave de registro do Windows que contém valores para o mecanismo de banco de dados do Jet.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-206">Estatísticas do Jet OLEDB:Reset ISAM</span><span class="sxs-lookup"><span data-stu-id="3ea6b-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="3ea6b-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-208">Indica se o esquema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS deve redefinir seus contadores de desempenho depois de retornar informações sobre desempenho.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="3ea6b-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="3ea6b-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-211">Indica o maior intervalo de tempo, em milissegundos, durante o qual o Jet poderá retardar as gravações assíncronas em disco quando o banco de dados estiver aberto em modo multiusuário.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="3ea6b-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="3ea6b-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-214">Indica o caminho e o nome do arquivo de informações do grupo de trabalho (banco de dados do sistema).</span><span class="sxs-lookup"><span data-stu-id="3ea6b-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-215">Modo de confirmação do Jet OLEDB:Transaction</span><span class="sxs-lookup"><span data-stu-id="3ea6b-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="3ea6b-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-217">Indica se o Jet deverá gravar dados em disco em modo síncrono ou assíncrono quando uma transação for confirmada.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="3ea6b-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="3ea6b-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-220">Indica se as alterações feitas em transações serão gravadas em modo síncrono ou assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="3ea6b-221">Propriedades de Recordset e Command específicas para provedor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="3ea6b-p112">O provedor Jet também oferece suporte a várias propriedades **Recordset** e **Command** específicas para provedor. Essas propriedades são acessadas e definidas por meio da coleção **Properties** do objeto **Recordset** ou **Command**. A tabela lista o nome da propriedade do ADO e, entre parênteses, o nome da propriedade do OLE DB correspondente.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-225">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="3ea6b-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-226">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ea6b-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-227">Transações de OLEDB:Bulk Jet</span><span class="sxs-lookup"><span data-stu-id="3ea6b-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="3ea6b-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p113">Indica se operações SQL em massa serão transacionadas. Grandes operações em massa podem falhar quando transacionadas devido aos atrasos de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-231">Cursores do Jet OLEDB:Enable Fat</span><span class="sxs-lookup"><span data-stu-id="3ea6b-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="3ea6b-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-233">Indica se o Jet deve armazenar várias linhas em cache ao preencher um conjunto de registros usando fontes remotas de linhas.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-234">Tamanho do Cache de Cursor do Jet OLEDB:Fat</span><span class="sxs-lookup"><span data-stu-id="3ea6b-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="3ea6b-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p114">Indica o número de linhas que serão armazenadas em cache quando o cache de linhas do repositório de dados remoto estiver sendo utilizado. Este valor será ignorado, a menos que <strong>Jet OLEDB:Enable Fat Cursors</strong> seja True.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-238">Jet OLEDB: inconsistente</span><span class="sxs-lookup"><span data-stu-id="3ea6b-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="3ea6b-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-240">Indica se os resultados de consultas permitem atualizações inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-241">Jet OLEDB: bloqueio de granularidade</span><span class="sxs-lookup"><span data-stu-id="3ea6b-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="3ea6b-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-243">Indica se uma tabela é aberta usando bloqueio no nível de linha.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-244">Instrução de passagem do Jet OLEDB:ODBC</span><span class="sxs-lookup"><span data-stu-id="3ea6b-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="3ea6b-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-246">Indica que o Jet deve passar o texto SQL de um objeto <strong>Command</strong> inalterado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-247">Operações do Jet OLEDB:Partial em massa</span><span class="sxs-lookup"><span data-stu-id="3ea6b-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="3ea6b-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-249">Indica o comportamento do Jet quando operações SQL DML falharem.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-250">Jet OLEDB:Pass por meio de consulta em massa-Op</span><span class="sxs-lookup"><span data-stu-id="3ea6b-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="3ea6b-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-252">Indica se as consultas que não retornam um <strong>Recordset</strong> são passadas inalteradas para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-253">Cadeia de ligação do Jet OLEDB:Pass por meio de consulta</span><span class="sxs-lookup"><span data-stu-id="3ea6b-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="3ea6b-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-p115">Indica a sequência de conexão do Jet utilizada para estabelecer a conexão com um repositório remoto de dados. Este valor será ignorado, a menos que <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> seja True.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-257">Jet OLEDB: armazenados consulta</span><span class="sxs-lookup"><span data-stu-id="3ea6b-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="3ea6b-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-259">Indica se o texto de comando deve ser interpretado como uma consulta armazenada em vez de um comando SQL.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-260">Jet OLEDB: validar regras em conjunto</span><span class="sxs-lookup"><span data-stu-id="3ea6b-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="3ea6b-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="3ea6b-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-262">Indica se as regras de validação do Jet serão avaliadas quando os dados das colunas forem definidos ou quando as alterações forem confirmadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ea6b-p116">Por padrão, o OLE DB Provider for Microsoft Jet abre bancos de dados do Microsoft Jet em modo de leitura/gravação. Para abrir um banco de dados em modo somente leitura, defina a propriedade [Mode](mode-property-ado.md) do objeto **Connection** do ADO como **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="3ea6b-265">Uso do objeto Command</span><span class="sxs-lookup"><span data-stu-id="3ea6b-265">Command Object Usage</span></span>

<span data-ttu-id="3ea6b-p117">O texto de comando do objeto [Command](command-object-ado.md) usa o dialeto Microsoft Jet SQL. Você pode especificar consultas que retornem linhas, consultas ação e nomes de tabelas no texto de comando; entretanto, não há suporte para procedimentos armazenados, que não devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="3ea6b-268">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-268">Recordset Behavior</span></span>

<span data-ttu-id="3ea6b-p118">O mecanismo de banco de dados do Microsoft Jet não oferece suporte a cursores dinâmicos. Portanto, o OLE DB Provider for Microsoft Jet não oferece suporte ao tipo de cursor **adLockDynamic**. Quando um cursor dinâmico é solicitado, o provedor retorna um cursor de conjunto de chaves e redefine a propriedade [CursorType](cursortype-property-ado.md) para indicar o tipo de [Recordset](recordset-object-ado.md) retornado. Além disso, quando um **Recordset** que pode ser atualizado é solicitado (**LockType** é **adLockOptimistic**, **adLockBatchOptimistic** ou **adLockPessimistic**), o provedor também retorna um cursor de conjunto de chaves e redefine a propriedade **CursorType**.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="3ea6b-273">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="3ea6b-273">Dynamic Properties</span></span>

<span data-ttu-id="3ea6b-274">O OLE DB Provider for Microsoft Jet insere várias propriedades dinâmicas na coleção **Properties** dos objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) e [Command](command-object-ado.md) não abertos.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="3ea6b-p119">As tabelas abaixo são um índice cruzado dos nomes do ADO e do OLE DB de cada propriedade dinâmica. A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você encontrará mais informações sobre essas propriedades na Referência do programador do OLE DB. Localize o nome da propriedade do OLE DB no Índice ou consulte o Apêndice C: propriedades do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="3ea6b-279">Propriedades dinâmicas de Connection</span><span class="sxs-lookup"><span data-stu-id="3ea6b-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="3ea6b-280">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-281">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="3ea6b-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-282">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3ea6b-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="3ea6b-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="3ea6b-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="3ea6b-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3ea6b-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="3ea6b-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="3ea6b-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="3ea6b-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="3ea6b-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="3ea6b-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="3ea6b-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="3ea6b-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="3ea6b-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="3ea6b-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="3ea6b-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="3ea6b-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="3ea6b-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3ea6b-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="3ea6b-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="3ea6b-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="3ea6b-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="3ea6b-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3ea6b-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="3ea6b-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="3ea6b-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="3ea6b-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="3ea6b-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="3ea6b-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="3ea6b-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="3ea6b-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="3ea6b-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-329">Mode</span><span class="sxs-lookup"><span data-stu-id="3ea6b-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="3ea6b-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="3ea6b-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3ea6b-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="3ea6b-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="3ea6b-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="3ea6b-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="3ea6b-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3ea6b-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="3ea6b-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="3ea6b-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="3ea6b-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="3ea6b-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="3ea6b-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-355">Password</span><span class="sxs-lookup"><span data-stu-id="3ea6b-355">Password</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="3ea6b-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="3ea6b-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="3ea6b-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3ea6b-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="3ea6b-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3ea6b-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="3ea6b-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="3ea6b-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="3ea6b-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="3ea6b-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="3ea6b-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="3ea6b-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="3ea6b-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="3ea6b-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="3ea6b-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="3ea6b-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="3ea6b-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="3ea6b-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="3ea6b-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="3ea6b-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="3ea6b-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="3ea6b-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="3ea6b-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="3ea6b-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="3ea6b-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-391">User ID</span><span class="sxs-lookup"><span data-stu-id="3ea6b-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="3ea6b-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-393">User Name</span><span class="sxs-lookup"><span data-stu-id="3ea6b-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="3ea6b-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="3ea6b-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="3ea6b-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="3ea6b-397">Propriedades dinâmicas do Recordset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="3ea6b-398">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-399">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="3ea6b-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-400">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3ea6b-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="3ea6b-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="3ea6b-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3ea6b-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="3ea6b-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="3ea6b-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="3ea6b-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="3ea6b-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="3ea6b-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="3ea6b-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="3ea6b-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="3ea6b-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="3ea6b-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="3ea6b-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="3ea6b-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3ea6b-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3ea6b-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="3ea6b-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="3ea6b-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3ea6b-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3ea6b-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3ea6b-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3ea6b-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="3ea6b-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3ea6b-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3ea6b-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-466">IStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="3ea6b-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="3ea6b-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="3ea6b-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="3ea6b-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="3ea6b-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="3ea6b-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="3ea6b-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="3ea6b-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="3ea6b-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3ea6b-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="3ea6b-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3ea6b-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="3ea6b-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="3ea6b-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="3ea6b-544">Propriedades dinâmicas do Command</span><span class="sxs-lookup"><span data-stu-id="3ea6b-544">Command Dynamic Properties</span></span>

<span data-ttu-id="3ea6b-545">As propriedades abaixo são adicionadas à coleção **Properties** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ea6b-546">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="3ea6b-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3ea6b-547">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3ea6b-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="3ea6b-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="3ea6b-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3ea6b-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="3ea6b-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="3ea6b-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="3ea6b-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="3ea6b-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="3ea6b-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="3ea6b-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="3ea6b-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="3ea6b-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3ea6b-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3ea6b-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="3ea6b-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="3ea6b-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="3ea6b-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3ea6b-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3ea6b-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3ea6b-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3ea6b-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="3ea6b-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3ea6b-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3ea6b-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="3ea6b-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-607">IStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="3ea6b-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3ea6b-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="3ea6b-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="3ea6b-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="3ea6b-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3ea6b-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="3ea6b-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="3ea6b-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="3ea6b-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="3ea6b-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="3ea6b-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="3ea6b-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="3ea6b-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="3ea6b-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="3ea6b-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="3ea6b-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3ea6b-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="3ea6b-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3ea6b-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="3ea6b-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="3ea6b-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="3ea6b-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="3ea6b-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="3ea6b-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="3ea6b-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ea6b-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="3ea6b-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="3ea6b-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ea6b-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3ea6b-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3ea6b-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3ea6b-687">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ea6b-687">See also</span></span>

<span data-ttu-id="3ea6b-688">Para obter detalhes específicos de implementação e informações funcionais sobre o OLE DB Provider for Microsoft Jet, consulte o OLE DB Provider para a documentação do Microsoft Jet no MDAC SDK.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

