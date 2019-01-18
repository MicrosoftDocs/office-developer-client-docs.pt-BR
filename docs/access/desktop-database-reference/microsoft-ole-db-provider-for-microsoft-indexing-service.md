---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba27bfdf6cc1317b441e626c61784e2c50b589f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716604"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="1459f-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span><span class="sxs-lookup"><span data-stu-id="1459f-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="1459f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1459f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1459f-104">O Microsoft OLE DB Provider for Microsoft Indexing Service fornece acesso programático de somente leitura aos dados de sistema e da web de arquivo indexados pela Microsoft Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="1459f-104">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="1459f-105">Os aplicativos do ADO podem emitir consultas SQL para recuperar informações sobre o conteúdo e as propriedades de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1459f-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="1459f-106">O provedor é de encadeamento livre e habilitado para unicode.</span><span class="sxs-lookup"><span data-stu-id="1459f-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="1459f-107">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="1459f-107">Connection String Parameters</span></span>

<span data-ttu-id="1459f-108">Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** para a propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="1459f-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="1459f-109">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1459f-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="1459f-110">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="1459f-110">Typical Connection String</span></span>

<span data-ttu-id="1459f-111">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="1459f-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="1459f-112">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="1459f-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1459f-113">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="1459f-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="1459f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1459f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1459f-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="1459f-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="1459f-p102">Especifica o Microsoft OLE DB Provider for Microsoft Indexing Service. Geralmente, é a única palavra-chave especificada na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="1459f-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-118"><strong>Fonte de dados</strong></span><span class="sxs-lookup"><span data-stu-id="1459f-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="1459f-p103">Especifica o nome de catálogo do Serviço de Indexação. Se esta palavra-chave não for especificada, será utilizado o catálogo padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="1459f-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-121"><strong>Identificador de localidade </strong></span><span class="sxs-lookup"><span data-stu-id="1459f-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="1459f-p104">Especifica um número único de 32 bits (por exemplo, 1033) que especifica as preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante. Se esta palavra-chave não for especificada, será utilizado o identificador de localidade padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="1459f-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="1459f-125">Texto de comando</span><span class="sxs-lookup"><span data-stu-id="1459f-125">Command Text</span></span>

<span data-ttu-id="1459f-p105">A sintaxe de consultas SQL do Serviço de Indexação consiste em extensões à instrução **SELECT** do SQL-92 e suas cláusulas **FROM** e **WHERE**. Os resultados da consulta são retornados pelos conjuntos de linhas do OLE DB, que podem ser consumidos pelo ADO e manipulados como objetos [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1459f-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="1459f-p106">Você pode pesquisar palavras ou frases exatas ou usar curingas para pesquisar padrões ou raízes de palavras. A lógica de pesquisa pode ser baseada em decisões booleanas, em termos balanceados ou na proximidade de outras palavras. Também é possível realizar pesquisas baseadas em "texto livre", que localizam coincidências com base no significado e não em palavras exatas.</span><span class="sxs-lookup"><span data-stu-id="1459f-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="1459f-131">O provedor não aceita chamadas de procedimento armazenado ou nomes simples de tabelas (por exemplo, a propriedade [CommandType](commandtype-property-ado.md) sempre será **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="1459f-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="1459f-132">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="1459f-132">Recordset Behavior</span></span>

<span data-ttu-id="1459f-133">As tabelas a seguir listam os recursos disponíveis em um objeto **Recordset** aberto com esse provedor.</span><span class="sxs-lookup"><span data-stu-id="1459f-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="1459f-134">Somente o tipo de cursor estático (**adOpenStatic**) está disponível.</span><span class="sxs-lookup"><span data-stu-id="1459f-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="1459f-135">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção [Properties](properties-collection-ado.md) de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="1459f-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="1459f-136">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="1459f-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1459f-137">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1459f-137">Property</span></span></p></th>
<th><p><span data-ttu-id="1459f-138">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1459f-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1459f-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="1459f-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-140">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="1459f-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-142">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="1459f-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-144">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="1459f-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-146">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-147"><a href="bookmark-property-ado.md">Indicador</a>\*</span><span class="sxs-lookup"><span data-stu-id="1459f-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="1459f-148">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="1459f-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-150">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="1459f-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-152">sempre <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="1459f-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="1459f-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-154">sempre <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="1459f-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="1459f-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-156">sempre <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="1459f-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="1459f-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-158">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-159"><a href="filter-property-ado.md">Filtro</a></span><span class="sxs-lookup"><span data-stu-id="1459f-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-160">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-161"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="1459f-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-162">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="1459f-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-164">não disponível</span><span class="sxs-lookup"><span data-stu-id="1459f-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="1459f-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-166">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="1459f-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-168">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="1459f-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-170">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="1459f-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-172">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-173"><a href="source-property-ado-recordset.md">Fonte</a></span><span class="sxs-lookup"><span data-stu-id="1459f-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-174">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1459f-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-175"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="1459f-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-176">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-177"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="1459f-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-178">somente leitura</span><span class="sxs-lookup"><span data-stu-id="1459f-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1459f-179">\*Indicadores devem estar habilitados no provedor para que este recurso exista no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1459f-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="1459f-180">Disponibilidade dos métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="1459f-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1459f-181">Método</span><span class="sxs-lookup"><span data-stu-id="1459f-181">Method</span></span></p></th>
<th><p><span data-ttu-id="1459f-182">Disponível?</span><span class="sxs-lookup"><span data-stu-id="1459f-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1459f-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="1459f-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-184">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-185"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="1459f-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-186">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="1459f-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-188">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="1459f-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-190">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="1459f-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-192">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="1459f-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-194">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-195"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="1459f-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-196">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="1459f-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-198">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="1459f-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-200">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="1459f-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-202">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="1459f-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-204">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1459f-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-206">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-207"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="1459f-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-208">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-209"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="1459f-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-210">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-211"><a href="supports-method-ado.md">Suporta</a></span><span class="sxs-lookup"><span data-stu-id="1459f-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-212">Sim</span><span class="sxs-lookup"><span data-stu-id="1459f-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459f-213"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="1459f-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-214">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1459f-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="1459f-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="1459f-216">Não</span><span class="sxs-lookup"><span data-stu-id="1459f-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1459f-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="1459f-217">See also</span></span>

<span data-ttu-id="1459f-218">Para obter detalhes específicos de implementação e informações funcionais sobre o Microsoft OLE DB Provider for Microsoft Indexing Service, consulte de referência o Microsoft OLE DB do programador.</span><span class="sxs-lookup"><span data-stu-id="1459f-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

