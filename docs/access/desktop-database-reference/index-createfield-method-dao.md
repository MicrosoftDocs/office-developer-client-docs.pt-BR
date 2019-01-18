---
title: Método Index.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703024"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="8a540-102">Método Index.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a540-102">Index.CreateField method (DAO)</span></span>

<span data-ttu-id="8a540-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a540-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a540-104">Cria um novo objeto **[Field](field-object-dao.md)** (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="8a540-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a540-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a540-105">Syntax</span></span>

<span data-ttu-id="8a540-106">*expressão* . CreateField (***nome***, ***tipo***, ***tamanho***)</span><span class="sxs-lookup"><span data-stu-id="8a540-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="8a540-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="8a540-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a540-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a540-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a540-109">Nome</span><span class="sxs-lookup"><span data-stu-id="8a540-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8a540-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="8a540-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8a540-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8a540-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8a540-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a540-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a540-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8a540-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8a540-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="8a540-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a540-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8a540-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8a540-p101">Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a540-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a540-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="8a540-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="8a540-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="8a540-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a540-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8a540-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8a540-121">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="8a540-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a540-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="8a540-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="8a540-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="8a540-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a540-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8a540-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8a540-125">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="8a540-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8a540-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8a540-126">Return value</span></span>

<span data-ttu-id="8a540-127">Field</span><span class="sxs-lookup"><span data-stu-id="8a540-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="8a540-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a540-128">Remarks</span></span>

<span data-ttu-id="8a540-p102">Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo de dados e o tamanho do campo. Se omitir uma ou mais dessas partes opcionais quando usar **CreateField**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o novo objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos individuais de propriedade para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8a540-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="8a540-133">Os argumentos de tipo e tamanho se aplicam somente aos objetos de **campo** em um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="8a540-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="8a540-134">Esses argumentos são ignorados quando um objeto **Field** é associado com um objeto **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="8a540-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="8a540-135">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="8a540-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="8a540-p104">Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Você não pode excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um índice que faz referência ao campo.</span><span class="sxs-lookup"><span data-stu-id="8a540-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

