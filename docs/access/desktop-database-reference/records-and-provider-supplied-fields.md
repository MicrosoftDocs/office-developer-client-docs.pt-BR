---
title: Registros e campos fornecidos pelo provedor
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e01d9dd1dce81911b11b7de8ca8c6ad5a19eaaf
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998319"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="edd54-102">Registros e campos fornecidos pelo provedor</span><span class="sxs-lookup"><span data-stu-id="edd54-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="edd54-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="edd54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edd54-104">Quando um objeto [Record](record-object-ado.md) é aberto, sua origem pode ser a linha atual de um [Recordset](recordset-object-ado.md) aberto, uma URL absoluta ou uma URL relativa em conjunto com um objeto [Connection](connection-object-ado.md) aberto.</span><span class="sxs-lookup"><span data-stu-id="edd54-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="edd54-105">Se **Record** for aberto a partir de um **Recordset**, a coleção **Fields** com o objeto [Record](fields-collection-ado.md) conterá todos os campos do **Recordset**, além de qualquer campo adicionado pelo provedor subjacente.</span><span class="sxs-lookup"><span data-stu-id="edd54-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="edd54-p101">O provedor pode inserir campos adicionais que funcionem como características complementares de **Record**. Como resultado, um **Record** poderá ter campos exclusivos que não façam parte de **Recordset** como um todo ou qualquer **Record** derivado de outra linha de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="edd54-p101">The provider may insert additional fields that serve as supplementary characteristics of the **Record**. As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="edd54-108">Por exemplo, todas as linhas de um **Recordset** derivado de uma fonte de dados de email talvez tenha colunas, tais como de fazer e da entidade.</span><span class="sxs-lookup"><span data-stu-id="edd54-108">For example, all rows of a **Recordset** derived from an email data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="edd54-109">Um **Record** derivado desse **Recordset** terá os mesmos campos.</span><span class="sxs-lookup"><span data-stu-id="edd54-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="edd54-110">Entretanto, o **Record** também pode ter outros campos exclusivos da mensagem específica representada por esse **Record**, como Anexo e Com cópia.</span><span class="sxs-lookup"><span data-stu-id="edd54-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="edd54-111">Embora o objeto **Record** e a linha atual de **Recordset** tenham os mesmos campos, eles são diferentes, pois os objetos **Record** e **Recordset** possuem métodos e propriedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="edd54-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="edd54-p103">Um mesmo campo mantido por **Record** e por **Recordset** pode ser modificado em um desses dois objetos. Entretanto, ele não pode ser excluído do objeto **Record**, embora o provedor subjacente possa permitir a configuração do campo como nulo.</span><span class="sxs-lookup"><span data-stu-id="edd54-p103">A field held in common by the **Record** and **Recordset** can be modified on either object. However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="edd54-p104">Depois que **Record** for aberto, você poderá adicionar campos por programação. Você também poderá excluir os campos adicionados, mas não poderá excluir campos do **Recordset** original.</span><span class="sxs-lookup"><span data-stu-id="edd54-p104">After the **Record** is opened, you can programmatically add fields. You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="edd54-p105">Também será permitido abrir o objeto **Record** diretamente de uma URL. Nesse caso, os campos adicionados a **Record** dependerão do provedor subjacente. No momento, a maioria dos provedores adiciona um conjunto de campos que descrevem a entidade representada por **Record**. Se a entidade consistir em um fluxo de bytes, como no caso de um arquivo simples, um objeto [Stream](stream-object-ado.md) geralmente poderá ser aberto a partir de **Record**.</span><span class="sxs-lookup"><span data-stu-id="edd54-p105">You may also open the **Record** object directly from a URL. In this case, the fields added to the **Record** depend on the underlying provider. Currently, most providers add a set of fields that describe the entity represented by the **Record**. If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="edd54-120">Campos especiais para provedores de fonte de documentos</span><span class="sxs-lookup"><span data-stu-id="edd54-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="edd54-p106">Uma classe especial de provedores, denominada *provedores de fonte de documentos*, gerencia pastas e documentos. Quando um objeto **Record** representa um documento ou um objeto **Recordset** representa uma pasta de documentos, o provedor de fonte de documentos preenche esses objetos com um conjunto exclusivo de campos que descrevem as características do documento, em vez do documento real. Em geral, um campo contém uma referência a **Stream** que representa o documento.</span><span class="sxs-lookup"><span data-stu-id="edd54-p106">A special class of providers, called *document source providers*, manages folders and documents. When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself. Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="edd54-124">Esses campos constituem um **record** ou um **recordset** de recurso e estão listados no [Apêndice A: Provedores](appendix-a-providers.md) para os provedores específicos que oferecem suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="edd54-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="edd54-p107">Duas constantes indexam a coleção **Fields** de um **Record** ou **Recordset** de recurso para a recuperação de um par de campos comumente utilizados. A propriedade **Value** do objeto [Field](value-property-ado.md) retorna o conteúdo desejado.</span><span class="sxs-lookup"><span data-stu-id="edd54-p107">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields. The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="edd54-p108">O campo acessado com a constante **adDefaultStream** contém um fluxo padrão associado ao objeto **Record** ou **Recordset**. O provedor atribui um fluxo padrão a um objeto.</span><span class="sxs-lookup"><span data-stu-id="edd54-p108">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object. The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="edd54-129">O campo acessado com a constante **adRecordURL** contém a URL absoluta que identifica o documento.</span><span class="sxs-lookup"><span data-stu-id="edd54-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="edd54-p109">Um provedor de fonte de documentos não oferece suporte à coleção [Properties](properties-collection-ado.md) dos objetos **Record** e **Field**. O conteúdo da coleção **Properties** é nulo para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="edd54-p109">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects. The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="edd54-p110">Um provedor de fonte de documentos pode adicionar uma propriedade específica de provedor, como **Datasource Type**, para identificar um provedor desse tipo. Para obter mais informações sobre como determinar o seu tipo de provedor, consulte a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="edd54-p110">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider. For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="edd54-134">Colunas do conjunto de registros de recurso</span><span class="sxs-lookup"><span data-stu-id="edd54-134">Resource Recordset Columns</span></span>

<span data-ttu-id="edd54-135">Um *conjunto de registros de recurso* consiste nas seguintes colunas.</span><span class="sxs-lookup"><span data-stu-id="edd54-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edd54-136">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="edd54-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="edd54-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="edd54-137">Type</span></span></p></th>
<th><p><span data-ttu-id="edd54-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="edd54-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edd54-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="edd54-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="edd54-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-p111">Somente leitura. Indica a URL do recurso.</span><span class="sxs-lookup"><span data-stu-id="edd54-p111">Read-only. Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="edd54-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="edd54-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-p112">Somente leitura. Indica a URL absoluta do registro pai.</span><span class="sxs-lookup"><span data-stu-id="edd54-p112">Read-only. Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="edd54-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="edd54-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-p113">Somente leitura. Indica a URL absoluta do recurso, que é a concatenação de PARENTNAME e PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="edd54-p113">Read-only. Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="edd54-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="edd54-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="edd54-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="edd54-p114">True se o recurso estiver oculto. Nenhuma linha será retornada, a menos que o comando que estiver criando o conjunto de linhas selecione explicitamente as linhas em que RESOURCE_ISHIDDEN seja True.</span><span class="sxs-lookup"><span data-stu-id="edd54-p114">True if the resource is hidden. No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="edd54-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="edd54-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="edd54-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="edd54-p115">True se o recurso for somente leitura. Qualquer tentativa de abrir esse recurso com DBBINDFLAG_WRITE não terá êxito com DB_E_READONLY. Esta propriedade poderá ser editada mesmo quando o recurso for aberto somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="edd54-p115">True if the resource is read-only. Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY. This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="edd54-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="edd54-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-162">Indica o uso provável do documento — por exemplo, um advogado do breve.</span><span class="sxs-lookup"><span data-stu-id="edd54-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="edd54-163">Isso poderá corresponder ao modelo do Office usado para criar o documento.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="edd54-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="edd54-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="edd54-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-166">Indica o tipo MIME do documento, que indica o formato como &quot;texto/html&quot;.'</span><span class="sxs-lookup"><span data-stu-id="edd54-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="edd54-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="edd54-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-169">Indica a linguagem na qual é armazenado o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="edd54-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="edd54-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="edd54-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="edd54-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="edd54-p117">Somente leitura. Indica uma estrutura FILETIME contendo a hora de criação do recurso, exibida no formato da hora universal coordenada (UTC).</span><span class="sxs-lookup"><span data-stu-id="edd54-p117">Read-only. Indicates a FILETIME structure containing the time the resource was created. The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="edd54-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="edd54-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="edd54-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="edd54-p118">Somente leitura. Indica uma estrutura FILETIME contendo a hora, em formato UTC, do último acesso ao recurso. Os membros de FILETIME terão o valor zero se o provedor não oferecer suporte a esse membro de hora.</span><span class="sxs-lookup"><span data-stu-id="edd54-p118">Read-only. Indicates a FILETIME structure containing the time that the resource was last accessed. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="edd54-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="edd54-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="edd54-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="edd54-p119">Somente leitura. Indica uma estrutura FILETIME contendo a hora, em formato UTC, da última gravação do recurso. Os membros de FILETIME terão o valor zero se o provedor não oferecer suporte a esse membro de hora.</span><span class="sxs-lookup"><span data-stu-id="edd54-p119">Read-only. Indicates a FILETIME structure containing the time that the resource was last written. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="edd54-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="edd54-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="edd54-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="edd54-p120">Somente leitura. Indica o tamanho, em bytes, do fluxo padrão do recurso.</span><span class="sxs-lookup"><span data-stu-id="edd54-p120">Read-only. Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="edd54-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="edd54-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="edd54-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="edd54-p121">Somente leitura. True se o recurso for uma coleção, por exemplo, um diretório. False se o recurso for um arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="edd54-p121">Read-only. True if the resource is a collection, such as a directory. False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="edd54-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="edd54-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="edd54-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="edd54-p122">True se o recurso for um documento estruturado. Caso contrário, será False. Pode ser uma coleção ou um arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="edd54-p122">True if the resource is a structured document. False if the resource is not a structured document. It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="edd54-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="edd54-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-p123">Somente leitura. Indica que o recurso contém uma URL para o documento simples padrão de uma pasta ou para um documento estruturado. Usado quando o fluxo padrão for solicitado de um recurso. Esta propriedade estará em branco para um arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="edd54-p123">Read-only. Indicates that this resource contains a URL to the default simple document of a folder or a structured document. Used when the default stream is requested from a resource. This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="edd54-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="edd54-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="edd54-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="edd54-p124">Somente leitura. Opcional. Indica o capítulo do conjunto de linhas contendo o filho do recurso. (O <em>OLE DB Provider for Internet Publishing</em> não usa esta coluna.)</span><span class="sxs-lookup"><span data-stu-id="edd54-p124">Read-only. Optional. Indicates the chapter of the rowset containing the children of the resource. (The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edd54-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="edd54-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="edd54-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="edd54-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="edd54-p125">Somente leitura. Indica o nome para exibição do recurso.</span><span class="sxs-lookup"><span data-stu-id="edd54-p125">Read-only. Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edd54-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="edd54-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="edd54-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="edd54-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="edd54-p126">Somente leitura. True se o recurso for a raiz de uma coleção ou de um documento estruturado.</span><span class="sxs-lookup"><span data-stu-id="edd54-p126">Read-only. True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>

