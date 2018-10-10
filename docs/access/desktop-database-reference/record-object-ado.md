---
title: Objeto Record (ADO)
TOCTitle: Record Object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c1071751df32fbfe89a4ee47e9c6a0613dce68e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464633"
---
# <a name="record-object-ado"></a><span data-ttu-id="efdf6-102">Objeto Record (ADO)</span><span class="sxs-lookup"><span data-stu-id="efdf6-102">Record Object (ADO)</span></span>


<span data-ttu-id="efdf6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="efdf6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="efdf6-104">Representa uma linha de um [Recordset](recordset-object-ado.md) ou do provedor de dados ou um objeto retornado pelo provedor de dados semi-estruturado, como um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="efdf6-104">Represents a row from a [Recordset](recordset-object-ado.md) or the data provider, or an object returned by a semi-structured data provider, such as a file or directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="efdf6-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="efdf6-105">Remarks</span></span>

<span data-ttu-id="efdf6-p101">Um objeto **Record** representa uma linha de dados e tem algumas similaridades conceituais com o **Recordset** de uma linha. Dependendo das capacidades do provedor, os objetos **Record** podem ser retornados diretamente do provedor, em vez de serem retornados do **Recordset** de uma linha, quando, por exemplo, é executada uma consulta SQL que seleciona somente uma linha; ou o objeto **Record** pode ser obtido diretamente de um objeto **Recordset**; ou um **Record** pode ser retornado diretamente de um provedor de dados semi-estruturados como o Microsoft Exchange OLE DB provider.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p101">A **Record** object represents one row of data, and has some conceptual similarities with a one-row **Recordset**. Depending upon the capabilities of your provider, **Record** objects may be returned directly from your provider instead of a one-row **Recordset**, for example when an SQL query that selects only one row is executed. Or, a **Record** object can be obtained directly from a **Recordset** object. Or, a **Record** can be returned directly from a provider to semi-structured data, such as the Microsoft Exchange OLE DB provider.</span></span>

<span data-ttu-id="efdf6-p102">Você pode exibir os campos associados ao objeto **Record** por meio da coleção [Fields](fields-collection-ado.md) no objeto **Record**. O ADO permite colunas com valor de objeto, incluindo **Recordset**, **SafeArray** e valores escalares na coleção **Fields** dos objetos **Record**.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p102">You can view the fields associated with the **Record** object by way of the [Fields](fields-collection-ado.md) collection on the **Record** object. ADO allows object-valued columns including **Recordset**, **SafeArray**, and scalar values in the **Fields** collection of **Record** objects.</span></span>

<span data-ttu-id="efdf6-112">Se o objeto **Record** representar uma linha em um **Recordset**, será possível retornar para esse **Recordset** original com a propriedade [Source](source-property-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-112">If the **Record** object represents a row in a **Recordset**, then it is possible to return to that original **Recordset** with the [Source](source-property-ado-record.md) property.</span></span>

<span data-ttu-id="efdf6-p103">O objeto **Record** também pode ser usado pelos provedores de dados semi-estruturados como o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) para modelar os espaços para nome em forma de árvore. Cada nó em uma árvore é um objeto **Record** com as colunas associadas. As colunas podem representar os atributos desse nó e outras informações relevantes. O objeto **Record** pode representar tanto um nó folha como um nó não folha na estrutura em árvore. Os nós não folha têm outros nós como seus conteúdos enquanto os nós folha não têm esses conteúdos. Geralmente, os nós folha contêm fluxos de dados binários enquanto os nós não folha também têm um fluxo binário padrão associado. As propriedades do objeto **Record** identificam o tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p103">The **Record** object can also be used by semi-structured data providers such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), to model tree-structured namespaces. Each node in the tree is a **Record** object with associated columns. The columns can represent the attributes of that node and other relevant information. The **Record** object can represent both a leaf node and a non-leaf node in the tree structure. Non-leaf nodes have other nodes as their contents while leaf nodes do not have such contents. Leaf nodes typically contain binary streams of data while non-leaf nodes may also have a default binary stream associated with them. Properties on the **Record** object identify the type of node.</span></span>

<span data-ttu-id="efdf6-p104">O objeto **Record** também representa uma forma alternativa de navegar hierarquicamente nos dados organizados. É possível criar um objeto **Record** para representar a raiz de uma subárvore em uma estrutura em árvore grande e os novos objetos **Record** podem ser abertos para representar nós filhos.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p104">The **Record** object also represents an alternative way for navigating hierarchically organized data. A **Record** object may be created to represent the root of a specific sub-tree in a large tree structure and new **Record** objects may be opened to represent child nodes.</span></span>

<span data-ttu-id="efdf6-122">Um recurso (por exemplo, um arquivo ou um diretório) pode ser identificado exclusivamente por uma URL absoluta.</span><span class="sxs-lookup"><span data-stu-id="efdf6-122">A resource (for example, a file or directory) can be uniquely identified by an absolute URL.</span></span> <span data-ttu-id="efdf6-123">Um objeto [Connection](connection-object-ado.md) será criado e definido de forma implícita como o objeto **Record**, quando o **Record** for aberto com uma URL absoluta.</span><span class="sxs-lookup"><span data-stu-id="efdf6-123">A [Connection](connection-object-ado.md) object is implicitly created and set to the **Record** object when the **Record** is opened with an absolute URL.</span></span> <span data-ttu-id="efdf6-124">Um objeto **Connection** pode ser definido de forma implícita como o objeto **Record** por meio da propriedade [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-124">A **Connection** object may explicitly be set to the **Record** object via the [ActiveConnection](activeconnection-property-ado.md) property.</span></span> <span data-ttu-id="efdf6-125">Os arquivos e diretórios acessíveis através do objeto de **Conexão** definem o *contexto* no qual as operações de **registro** podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="efdf6-125">The files and directories accessible via the **Connection** object define the *context* in which **Record** operations may occur.</span></span>

<span data-ttu-id="efdf6-126">A modificação dos dados e os métodos de navegação no objeto **Record** também aceitam uma URL relativa, que localiza um recurso usando uma URL absoluta ou o contexto do objeto **Connection** como um ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="efdf6-126">Data modification and navigation methods on the **Record** object also accept a relative URL, which locates a resource using an absolute URL or the **Connection** object context as a starting point.</span></span>


> [!NOTE]
> <P><span data-ttu-id="efdf6-p106">[!OBSERVAçãO] As URLs que usam o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs absolutos e relativos</A>.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p106">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>



<span data-ttu-id="efdf6-p107">Um objeto **Connection** está associado a cada objeto **Record**. Por esse motivo, as operações do objeto **Record** podem fazer parte de uma operação pela chamada dos métodos de transação do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="efdf6-p107">A **Connection** object is associated with each **Record** object. Therefore, **Record** object operations can be part of a transaction by invoking **Connection** object transaction methods.</span></span>

<span data-ttu-id="efdf6-131">O objeto **Record** não oferecer suporte aos eventos ADO e, por esse motivo, não responderá às notificações.</span><span class="sxs-lookup"><span data-stu-id="efdf6-131">The **Record** object does not support ADO events, and therefore will not respond to notifications.</span></span>

<span data-ttu-id="efdf6-132">Com os métodos e as propriedades de um objeto **Record**, é possível fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="efdf6-132">With the methods and properties of a **Record** object, you can do the following:</span></span>

  - <span data-ttu-id="efdf6-133">Definir ou retornar o objeto **Connection** associado à propriedade [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-133">Set or return the associated **Connection** object with the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="efdf6-134">Indicar as permissões de acesso à propriedade [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-134">Indicate access permissions with the [Mode](mode-property-ado.md) property.</span></span>

  - <span data-ttu-id="efdf6-135">Retornar a URL do diretório, se houver, que contém o recurso representado pelo **Record** com a propriedade [ParentURL](parenturl-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-135">Return the URL of the directory, if any, that contains the resource represented by the **Record** with the [ParentURL](parenturl-property-ado.md) property.</span></span>

  - <span data-ttu-id="efdf6-136">Indicar a URL absoluta, a URL relativa ou o **Recordset** a partir do qual o **Record** é derivado com a propriedade [Source](source-property-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-136">Indicate the absolute URL, relative URL, or **Recordset** from which the **Record** is derived with the [Source](source-property-ado-record.md) property.</span></span>

  - <span data-ttu-id="efdf6-137">Indicar o status atual do **Record** com a propriedade [State](state-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-137">Indicate the current status of the **Record** with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="efdf6-138">Indicar o tipo de **Record** — *simples*, *coleção* ou *documento estruturado* — com a propriedade [RecordType](recordtype-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-138">Indicate the type of **Record** — *simple*, *collection*, or *structured document* — with the [RecordType](recordtype-property-ado.md) property.</span></span>

  - <span data-ttu-id="efdf6-139">Suspender a execução de uma operação assíncrona com o método [Cancel](cancel-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-139">Halt execution of an asynchronous operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-140">Desassociar o **Record** de uma fonte de dados com o método [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-140">Disassociate the **Record** from a data source with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-141">Copiar o arquivo ou o diretório representado por um **Record** para outro local com o método [CopyRecord](copyrecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-141">Copy the file or directory represented by a **Record** to another location with the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-142">Excluir o arquivo ou o diretório e os subdiretórios, representado por um **Record** com o método [DeleteRecord](deleterecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-142">Delete the file, or directory and subdirectories, represented by a **Record** with the [DeleteRecord](deleterecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-143">Abrir um **Recordset** contendo linhas que representam os subdiretórios e os arquivos da entidade representados pelo **Record** com o método [GetChildren](getchildren-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-143">Open a **Recordset** containing rows that represent the subdirectories and files of the entity represented by the **Record** with the [GetChildren](getchildren-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-144">Mover (renomear) o arquivo ou o diretório e os subdiretórios, representado por um **Record** para outro local com o método [MoveRecord](moverecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-144">Move (rename) the file, or directory and subdirectories, represented by a **Record** to another location with the [MoveRecord](moverecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="efdf6-145">Associar o **Record** com uma fonte de dados existente ou criar um novo arquivo ou diretório com o método [Open](open-method-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="efdf6-145">Associate the **Record** with an existing data source, or create a new file or directory with the [Open](open-method-ado-record.md) method.</span></span>

