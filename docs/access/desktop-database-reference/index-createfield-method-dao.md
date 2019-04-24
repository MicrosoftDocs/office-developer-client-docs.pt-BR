---
title: Método index. CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291828"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="c4099-102">Método index. CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4099-102">Index.CreateField method (DAO)</span></span>

<span data-ttu-id="c4099-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4099-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4099-104">Cria um novo objeto **[Field](field-object-dao.md)** (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c4099-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4099-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4099-105">Syntax</span></span>

<span data-ttu-id="c4099-106">*expressão* . CreateField (***nome***, ***tipo***, ***tamanho***)</span><span class="sxs-lookup"><span data-stu-id="c4099-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="c4099-107">*expressão* Uma variável que representa um objeto **index** .</span><span class="sxs-lookup"><span data-stu-id="c4099-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4099-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4099-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4099-109">Nome</span><span class="sxs-lookup"><span data-stu-id="c4099-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c4099-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="c4099-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c4099-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c4099-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c4099-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4099-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4099-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="c4099-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="c4099-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="c4099-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4099-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4099-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4099-116">Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4099-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="c4099-117">Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes de <strong>campo</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="c4099-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4099-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="c4099-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="c4099-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="c4099-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4099-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4099-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4099-121">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="c4099-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4099-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="c4099-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="c4099-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="c4099-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4099-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4099-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4099-125">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="c4099-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="c4099-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c4099-126">Return value</span></span>

<span data-ttu-id="c4099-127">Campo</span><span class="sxs-lookup"><span data-stu-id="c4099-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="c4099-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4099-128">Remarks</span></span>

<span data-ttu-id="c4099-p102">Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo dos dados e o tamanho do campo. Se você omitir uma ou mais das partes opcionais ao utilizar **CreateField**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o novo objeto, será possível alterar algumas, mas não todas as suas configurações de propriedade. Consulte os tópicos de propriedade individuais para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c4099-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="c4099-133">Os argumentos Type e Size aplicam-se somente aos objetos **Field** em um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="c4099-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="c4099-134">Esses argumentos serão ignorados quando o objeto **Field** for associado a um objeto **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="c4099-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="c4099-135">Se Name se referir a um objeto que já é um membro da coleção, ocorrerá um erro em tempo de execução quando você usar o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="c4099-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="c4099-p104">Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Não é possível excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um index que faça referência ao campo.</span><span class="sxs-lookup"><span data-stu-id="c4099-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

