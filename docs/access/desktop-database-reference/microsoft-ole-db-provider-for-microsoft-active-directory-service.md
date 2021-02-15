---
title: Microsoft OLE DB Provider for Microsoft Active Directory Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288936"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="51fc5-102">Provedor Microsoft OLE DB para Microsoft Active Directory Service</span><span class="sxs-lookup"><span data-stu-id="51fc5-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="51fc5-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51fc5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51fc5-p101">O provedor ADSI (Interfaces de Serviços do Active Directory) da Microsoft permite que o ADO conecte-se a serviços de diretório heterogêneos por meio de ADSI. Isso fornece aos aplicativos do ADO acesso somente leitura aos serviços de diretório do Microsoft Windows NT 4.0 e Microsoft Windows 2000, além de qualquer serviço de diretório compatível com o LDAP e os Serviços de Diretório da Novell. O ADSI em si é baseado em um modelo de provedor, portanto, se houver um novo provedor fornecendo acesso a outro diretório, o aplicativo do ADO poderá acessá-lo sem qualquer problema. O provedor ADSI é de encadeamento livre e habilitado para unicode.</span><span class="sxs-lookup"><span data-stu-id="51fc5-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="51fc5-108">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="51fc5-108">Connection String Parameters</span></span>

<span data-ttu-id="51fc5-109">Para conectar-se a esse provedor, defina o argumento **Provider** da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="51fc5-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="51fc5-110">A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51fc5-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="51fc5-111">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="51fc5-111">Typical Connection String</span></span>

<span data-ttu-id="51fc5-112">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="51fc5-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="51fc5-113">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="51fc5-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51fc5-114">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="51fc5-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="51fc5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="51fc5-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="51fc5-117">Especifica o Microsoft OLE DB Provider for Microsoft Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="51fc5-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="51fc5-119">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="51fc5-119">Specifies the user name.</span></span> <span data-ttu-id="51fc5-120">Se essa palavra-chave for omitida, o logon atual será utilizado.</span><span class="sxs-lookup"><span data-stu-id="51fc5-120">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="51fc5-122">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="51fc5-122">Specifies the user password.</span></span> <span data-ttu-id="51fc5-123">Se essa palavra-chave for omitida, o logon atual será utilizado.</span><span class="sxs-lookup"><span data-stu-id="51fc5-123">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51fc5-124">**Texto de comando**</span><span class="sxs-lookup"><span data-stu-id="51fc5-124">**Command Text**</span></span>

<span data-ttu-id="51fc5-125">Uma sequência de texto de comando de quatro partes é reconhecida pelo provedor na seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="51fc5-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51fc5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="51fc5-126">Value</span></span></p></th>
<th><p><span data-ttu-id="51fc5-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="51fc5-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-128"><em>Raiz</em></span><span class="sxs-lookup"><span data-stu-id="51fc5-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="51fc5-129">Indica o objeto <strong>ADsPath</strong> a partir do qual iniciar a pesquisa (isto é, a raiz para a pesquisa).</span><span class="sxs-lookup"><span data-stu-id="51fc5-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-130"><em>Filtro</em></span><span class="sxs-lookup"><span data-stu-id="51fc5-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="51fc5-131">Indica o filtro da pesquisa no formato RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="51fc5-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-132"><em>Atributos</em></span><span class="sxs-lookup"><span data-stu-id="51fc5-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="51fc5-133">Indica uma lista de atributos a ser retornada, delimitada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="51fc5-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="51fc5-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="51fc5-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="51fc5-135">Optional.</span></span> <span data-ttu-id="51fc5-136">Uma <strong>String</strong> que especifica o escopo da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="51fc5-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="51fc5-137">Pode ser um dos seguintes: Base — pesquisa somente o objeto base (raiz da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="51fc5-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="51fc5-138">OneLevel — Pesquisa apenas um nível.</span><span class="sxs-lookup"><span data-stu-id="51fc5-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="51fc5-139">Subárvore — Pesquisa a subárvore inteira.</span><span class="sxs-lookup"><span data-stu-id="51fc5-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51fc5-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51fc5-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="51fc5-p105">O provedor também oferece suporte à SQL SELECT para o texto de comando. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51fc5-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="51fc5-p106">O provedor não aceita chamadas de procedimento armazenado ou nomes simples de tabelas (por exemplo, a propriedade [CommandType](commandtype-property-ado.md) sempre será **adCmdText**). Consulte a documentação das Interfaces de Serviços do Active Directory para obter uma descrição mais completa dos elementos do texto de comando.</span><span class="sxs-lookup"><span data-stu-id="51fc5-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="51fc5-145">Comportamento do Recordset</span><span class="sxs-lookup"><span data-stu-id="51fc5-145">Recordset Behavior</span></span>

<span data-ttu-id="51fc5-146">As tabelas a seguir relacionam os recursos disponíveis em um objeto [Recordset](recordset-object-ado.md) aberto com este provedor.</span><span class="sxs-lookup"><span data-stu-id="51fc5-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="51fc5-147">Somente o tipo de cursor Estático (**adOpenStatic**) está disponível.</span><span class="sxs-lookup"><span data-stu-id="51fc5-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="51fc5-148">Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção [Properties](properties-collection-ado.md) de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.</span><span class="sxs-lookup"><span data-stu-id="51fc5-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="51fc5-149">Disponibilidade das propriedades padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="51fc5-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51fc5-150">Propriedade</span><span class="sxs-lookup"><span data-stu-id="51fc5-150">Property</span></span></p></th>
<th><p><span data-ttu-id="51fc5-151">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="51fc5-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-153">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-155">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-157">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-159">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-161">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-163">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-165">sempre <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-167">sempre <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-169">sempre <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="51fc5-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-171">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-172"><a href="filter-property-ado.md">Filtro</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-173">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-175">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-177">não disponível</span><span class="sxs-lookup"><span data-stu-id="51fc5-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-179">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-181">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-183">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-185">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-186"><a href="source-property-ado-recordset.md">Fonte</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-187">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51fc5-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-189">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-190"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-191">somente leitura</span><span class="sxs-lookup"><span data-stu-id="51fc5-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51fc5-192">Disponibilidade de métodos padrão do **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="51fc5-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51fc5-193">Método</span><span class="sxs-lookup"><span data-stu-id="51fc5-193">Method</span></span></p></th>
<th><p><span data-ttu-id="51fc5-194">Disponível?</span><span class="sxs-lookup"><span data-stu-id="51fc5-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-196">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-198">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-200">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-202">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-204">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-206">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-208">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-210">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-211"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-212">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-214">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-216">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-218">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-220">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-222">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-224">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-226">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-228">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-229"><a href="supports-method-ado.md">Oferece suporte</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-230">Sim</span><span class="sxs-lookup"><span data-stu-id="51fc5-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51fc5-231"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-232">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51fc5-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="51fc5-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="51fc5-234">Não</span><span class="sxs-lookup"><span data-stu-id="51fc5-234">No</span></span></p></td>
</tr>
</tbody>
</table>

