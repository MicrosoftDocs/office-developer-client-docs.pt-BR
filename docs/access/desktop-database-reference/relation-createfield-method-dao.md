---
title: Método Relation.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d86230f99afb95d121ea683ed4324d361b77757
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602892"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="704a2-102">Método Relation.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="704a2-102">Relation.CreateField Method (DAO)</span></span>


<span data-ttu-id="704a2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="704a2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="704a2-104">Cria um novo objeto **[Field](field-object-dao.md)** (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="704a2-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="704a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="704a2-105">Syntax</span></span>

<span data-ttu-id="704a2-106">*expressão* . CreateField (***nome***, ***tipo***, ***tamanho***)</span><span class="sxs-lookup"><span data-stu-id="704a2-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="704a2-107">*expressão* Uma variável que representa um objeto **Relation** .</span><span class="sxs-lookup"><span data-stu-id="704a2-107">*expression* A variable that represents a **Relation** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="704a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="704a2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="704a2-109">Nome</span><span class="sxs-lookup"><span data-stu-id="704a2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="704a2-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="704a2-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="704a2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="704a2-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="704a2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="704a2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="704a2-113">Name</span><span class="sxs-lookup"><span data-stu-id="704a2-113">Name</span></span></p></td>
<td><p><span data-ttu-id="704a2-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="704a2-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="704a2-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="704a2-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="704a2-p101">Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="704a2-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="704a2-118">Type</span><span class="sxs-lookup"><span data-stu-id="704a2-118">Type</span></span></p></td>
<td><p><span data-ttu-id="704a2-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="704a2-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="704a2-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="704a2-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="704a2-121">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="704a2-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="704a2-122">Size</span><span class="sxs-lookup"><span data-stu-id="704a2-122">Size</span></span></p></td>
<td><p><span data-ttu-id="704a2-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="704a2-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="704a2-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="704a2-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="704a2-125">O argumento não tem suporte neste objeto.</span><span class="sxs-lookup"><span data-stu-id="704a2-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="704a2-126"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="704a2-126"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="704a2-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="704a2-127">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="704a2-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="704a2-128">Return value</span></span>
>>>>>>> <span data-ttu-id="704a2-129">mestre</span><span class="sxs-lookup"><span data-stu-id="704a2-129">master</span></span>

<span data-ttu-id="704a2-130">Field</span><span class="sxs-lookup"><span data-stu-id="704a2-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="704a2-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="704a2-131">Remarks</span></span>

<span data-ttu-id="704a2-p102">Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo de dados e o tamanho do campo. Se omitir uma ou mais dessas partes opcionais quando usar **CreateField**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o novo objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos individuais de propriedade para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="704a2-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="704a2-136">Os argumentos de tipo e tamanho se aplicam somente aos objetos de **campo** em um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="704a2-136">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="704a2-137">Esses argumentos são ignorados quando um objeto **Field** é associado com um objeto **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="704a2-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="704a2-138">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="704a2-138">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="704a2-p104">Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Você não pode excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um índice que faz referência ao campo.</span><span class="sxs-lookup"><span data-stu-id="704a2-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

