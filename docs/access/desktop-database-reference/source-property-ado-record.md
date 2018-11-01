---
title: Propriedade Source (Record do ADO)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e0157bc81e3f7efdb2227b5c5a9e2bc3642a7d2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883950"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="862c8-102">Propriedade Source (Record do ADO)</span><span class="sxs-lookup"><span data-stu-id="862c8-102">Source Property (ADO Record)</span></span>


<span data-ttu-id="862c8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="862c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="862c8-104">Indica a fonte de dados ou o objeto representado pelo [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="862c8-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="862c8-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="862c8-105">Settings and return values</span></span>

<span data-ttu-id="862c8-106">Define ou retorna um valor **Variant** que indica a entidade representada pelo **Record**.</span><span class="sxs-lookup"><span data-stu-id="862c8-106">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="862c8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="862c8-107">Remarks</span></span>

<span data-ttu-id="862c8-108">A propriedade **Source** retorna o argumento de *fonte* do objeto **Record** do método [Open](open-method-ado-record.md) .</span><span class="sxs-lookup"><span data-stu-id="862c8-108">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="862c8-109">Ela pode conter uma cadeia de caracteres de URL absoluta ou relativa.</span><span class="sxs-lookup"><span data-stu-id="862c8-109">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="862c8-110">Uma URL absoluta pode ser utilizada sem a definição da propriedade [ActiveConnection](activeconnection-property-ado.md) para abrir diretamente o objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="862c8-110">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="862c8-111">Neste caso, será criado um objeto **Connection** implícito.</span><span class="sxs-lookup"><span data-stu-id="862c8-111">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="862c8-112">A propriedade **Source** também pode conter uma referência a um **Recordset** já aberto, que abre um objeto **Record** representando a linha atual no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="862c8-112">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="862c8-113">A propriedade **Source** também pode conter uma referência a um objeto [Command](command-object-ado.md), que retorna uma única linha de dados do provedor.</span><span class="sxs-lookup"><span data-stu-id="862c8-113">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="862c8-p102">Se a propriedade **ActiveConnection** também for definida, então a propriedade **Source** deverá apontar para algum objeto que exista dentro do escopo dessa conexão. Por exemplo, namespaces em árvore estruturada, se a propriedade **Source** contiver uma URL absoluta, ela deverá apontar para um nó que exista dentro do escopo do nó identificado pela URL na sequência de conexão. Se a propriedade **Source** contiver uma URL relativa, ela será validada no conjunto de contexto pela propriedade **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="862c8-p102">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection. For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string. If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="862c8-117">A propriedade **Source** será leitura/gravação enquanto o objeto **Record** estiver fechado e somente leitura enquanto o objeto **Record** estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="862c8-117">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

> [!NOTE]
> <span data-ttu-id="862c8-118">[!OBSERVAçãO] As URLs que estiverem utilizando o esquema http invocarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="862c8-118">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="862c8-119">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="862c8-119">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


