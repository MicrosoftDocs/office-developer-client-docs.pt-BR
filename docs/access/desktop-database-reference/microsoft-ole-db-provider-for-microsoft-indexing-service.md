---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e41633ddb2730af66ddeee400ad035d5a17ed90d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607050"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="d9204-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span><span class="sxs-lookup"><span data-stu-id="d9204-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="d9204-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9204-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9204-104"><<<<<<< Cabeça o Microsoft OLE DB Provider for Microsoft Indexing Service fornece acesso programático de somente leitura para o sistema de arquivos e dados da Web indexados pela Microsoft Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d9204-104"><<<<<<< HEAD The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="d9204-105">Os aplicativos do ADO podem emitir consultas SQL para recuperar informações sobre o conteúdo e as propriedades de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d9204-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
<span data-ttu-id="d9204-106">=== O Microsoft OLE DB Provider for Microsoft Indexing Service fornece acesso programático de somente leitura aos dados de sistema e da web de arquivo indexados pela Microsoft Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d9204-106">======= The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="d9204-107">Os aplicativos do ADO podem emitir consultas SQL para recuperar informações sobre o conteúdo e as propriedades de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d9204-107">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
>>>>>>> <span data-ttu-id="d9204-108">mestre</span><span class="sxs-lookup"><span data-stu-id="d9204-108">master</span></span>

<span data-ttu-id="d9204-109">O provedor é de encadeamento livre e habilitado para unicode.</span><span class="sxs-lookup"><span data-stu-id="d9204-109">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="d9204-110">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="d9204-110">Connection String Parameters</span></span>

<span data-ttu-id="d9204-111">Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** para a propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="d9204-111">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="d9204-112">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9204-112">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="d9204-113">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="d9204-113">Typical Connection String</span></span>

<span data-ttu-id="d9204-114">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="d9204-114">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="d9204-115">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="d9204-115">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9204-116">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="d9204-116">Keyword</span></span></p></th>
<th><p><span data-ttu-id="d9204-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9204-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9204-118"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d9204-118"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d9204-p102">Especifica o Microsoft OLE DB Provider for Microsoft Indexing Service. Geralmente, é a única palavra-chave especificada na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="d9204-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-121"><strong>Fonte de dados</strong></span><span class="sxs-lookup"><span data-stu-id="d9204-121"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="d9204-p103">Especifica o nome de catálogo do Serviço de Indexação. Se esta palavra-chave não for especificada, será utilizado o catálogo padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="d9204-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-124"><strong>Identificador de localidade </strong></span><span class="sxs-lookup"><span data-stu-id="d9204-124"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="d9204-p104">Especifica um número único de 32 bits (por exemplo, 1033) que especifica as preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante. Se esta palavra-chave não for especificada, será utilizado o identificador de localidade padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="d9204-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="d9204-128">Texto de comando</span><span class="sxs-lookup"><span data-stu-id="d9204-128">Command Text</span></span>

<span data-ttu-id="d9204-p105">A sintaxe de consultas SQL do Serviço de Indexação consiste em extensões à instrução **SELECT** do SQL-92 e suas cláusulas **FROM** e **WHERE**. Os resultados da consulta são retornados pelos conjuntos de linhas do OLE DB, que podem ser consumidos pelo ADO e manipulados como objetos [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d9204-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="d9204-p106">Você pode pesquisar palavras ou frases exatas ou usar curingas para pesquisar padrões ou raízes de palavras. A lógica de pesquisa pode ser baseada em decisões booleanas, em termos balanceados ou na proximidade de outras palavras. Também é possível realizar pesquisas baseadas em "texto livre", que localizam coincidências com base no significado e não em palavras exatas.</span><span class="sxs-lookup"><span data-stu-id="d9204-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="d9204-134">O provedor não aceita chamadas de procedimento armazenado ou nomes simples de tabelas (por exemplo, a propriedade [CommandType](commandtype-property-ado.md) sempre será **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="d9204-134">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="d9204-135">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="d9204-135">Recordset Behavior</span></span>

<span data-ttu-id="d9204-136">As tabelas a seguir listam os recursos disponíveis em um objeto **Recordset** aberto com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="d9204-136">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="d9204-137">Somente o tipo de cursor estático (**adOpenStatic**) está disponível.</span><span class="sxs-lookup"><span data-stu-id="d9204-137">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="d9204-138">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção [Properties](properties-collection-ado.md) de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="d9204-138">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="d9204-139">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="d9204-139">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9204-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d9204-140">Property</span></span></p></th>
<th><p><span data-ttu-id="d9204-141">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d9204-141">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9204-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="d9204-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-143">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-143">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="d9204-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-145">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-145">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="d9204-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-147">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-147">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-148"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="d9204-148"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-149">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-149">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-150"><a href="bookmark-property-ado.md">Indicador</a>\*</span><span class="sxs-lookup"><span data-stu-id="d9204-150"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="d9204-151">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-151">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-152"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="d9204-152"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-153">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-153">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="d9204-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-155">sempre <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="d9204-155">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-156"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="d9204-156"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-157">sempre <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="d9204-157">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-158"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="d9204-158"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-159">sempre <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="d9204-159">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-160"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="d9204-160"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-161">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-161">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-162"><a href="filter-property-ado.md">Filtrar</a></span><span class="sxs-lookup"><span data-stu-id="d9204-162"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-163">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-163">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-164"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="d9204-164"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-165">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-165">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="d9204-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-167">não disponível</span><span class="sxs-lookup"><span data-stu-id="d9204-167">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="d9204-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-169">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-169">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-170"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="d9204-170"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-171">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-171">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-172"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="d9204-172"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-173">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-173">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-174"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="d9204-174"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-175">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-175">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-176"><a href="source-property-ado-recordset.md">Origem</a></span><span class="sxs-lookup"><span data-stu-id="d9204-176"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-177">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9204-177">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-178"><a href="state-property-ado.md">Estado</a></span><span class="sxs-lookup"><span data-stu-id="d9204-178"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-179">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-179">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-180"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="d9204-180"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-181">somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9204-181">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d9204-182">\*Indicadores devem estar habilitados no provedor para que este recurso exista no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d9204-182">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="d9204-183">Disponibilidade dos métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="d9204-183">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9204-184">Método</span><span class="sxs-lookup"><span data-stu-id="d9204-184">Method</span></span></p></th>
<th><p><span data-ttu-id="d9204-185">Disponível?</span><span class="sxs-lookup"><span data-stu-id="d9204-185">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9204-186"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="d9204-186"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-187">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-187">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-188"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="d9204-188"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-189">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-189">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="d9204-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-191">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-191">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="d9204-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-193">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-193">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-194"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="d9204-194"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-195">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-195">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-196"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="d9204-196"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-197">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-197">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-198"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="d9204-198"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-199">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-199">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-200"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="d9204-200"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-201">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-201">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-202"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="d9204-202"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-203">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="d9204-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-205">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="d9204-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-207">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-207">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-208"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="d9204-208"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-209">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-209">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-210"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="d9204-210"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-211">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-211">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-212"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="d9204-212"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-213">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-213">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-214"><a href="supports-method-ado.md">Suporta</a></span><span class="sxs-lookup"><span data-stu-id="d9204-214"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-215">Sim</span><span class="sxs-lookup"><span data-stu-id="d9204-215">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9204-216"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="d9204-216"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-217">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-217">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9204-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="d9204-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="d9204-219">Não</span><span class="sxs-lookup"><span data-stu-id="d9204-219">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d9204-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9204-220">See also</span></span>

<span data-ttu-id="d9204-221">Para obter detalhes específicos de implementação e informações funcionais sobre o Microsoft OLE DB Provider for Microsoft Indexing Service, consulte de referência o Microsoft OLE DB do programador.</span><span class="sxs-lookup"><span data-stu-id="d9204-221">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

