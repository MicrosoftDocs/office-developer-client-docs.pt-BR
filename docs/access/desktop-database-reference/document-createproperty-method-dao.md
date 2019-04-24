---
title: Método Document. createProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d1e2e2200953580406dded7d5c014b533129b133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293816"
---
# <a name="documentcreateproperty-method-dao"></a><span data-ttu-id="0f91a-102">Método Document. createProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f91a-102">Document.CreateProperty method (DAO)</span></span>

<span data-ttu-id="0f91a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f91a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f91a-104">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0f91a-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f91a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f91a-105">Syntax</span></span>

<span data-ttu-id="0f91a-106">*expressão* . CreateProperty (***nome***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="0f91a-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="0f91a-107">*expressão* Uma variável que representa um objeto **Document** .</span><span class="sxs-lookup"><span data-stu-id="0f91a-107">*expression* A variable that represents a **Document** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f91a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f91a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f91a-109">Nome</span><span class="sxs-lookup"><span data-stu-id="0f91a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0f91a-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="0f91a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="0f91a-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f91a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="0f91a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f91a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f91a-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="0f91a-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="0f91a-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f91a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f91a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f91a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f91a-116">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f91a-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="0f91a-117">Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f91a-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f91a-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="0f91a-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="0f91a-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f91a-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f91a-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f91a-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f91a-121">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f91a-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="0f91a-122">Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="0f91a-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f91a-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="0f91a-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="0f91a-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f91a-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f91a-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f91a-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f91a-126">Um <strong>Variant</strong> que contém o valor inicial da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0f91a-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="0f91a-127">Consulte a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0f91a-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f91a-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="0f91a-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="0f91a-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f91a-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f91a-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f91a-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f91a-131">Um <strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica se <strong>Property</strong> é ou não um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="0f91a-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="0f91a-132">O padrão é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f91a-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="0f91a-133">Se DDL for <strong>true</strong>, os usuários não poderão alterar ou excluir este objeto <strong>Property</strong> , a menos que tenham permissão <strong>dbSecWriteDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f91a-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="0f91a-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0f91a-134">Return value</span></span>

<span data-ttu-id="0f91a-135">Propriedade	</span><span class="sxs-lookup"><span data-stu-id="0f91a-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="0f91a-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f91a-136">Remarks</span></span>

<span data-ttu-id="0f91a-137">Você pode criar um objeto **Property** definido pelo usuário na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="0f91a-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="0f91a-p105">Se você omitir uma ou mais das partes opcionais ao utilizar **CreateProperty**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas, as configurações de propriedade. Consulte os tópicos de propriedade **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0f91a-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="0f91a-141">Se Name se referir a um objeto que já é um membro da coleção, ocorrerá um erro em tempo de execução quando você usar o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="0f91a-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="0f91a-142">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**.</span><span class="sxs-lookup"><span data-stu-id="0f91a-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="0f91a-143">Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="0f91a-143">You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="0f91a-144">Se você omitir o argumento DDL, ele será padronizado como false (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="0f91a-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="0f91a-145">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar o objeto **Property** que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="0f91a-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


