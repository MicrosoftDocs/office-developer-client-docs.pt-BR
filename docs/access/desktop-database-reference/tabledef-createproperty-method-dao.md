---
title: Método TableDef.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3018bf8cc9a62cb866b35992e25ecb1f8f41514f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308418"
---
# <a name="tabledefcreateproperty-method-dao"></a><span data-ttu-id="cdf63-102">Método TableDef.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="cdf63-102">TableDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="cdf63-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdf63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdf63-104">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cdf63-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdf63-105">Syntax</span></span>

<span data-ttu-id="cdf63-106">*expressão* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="cdf63-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="cdf63-107">*expressão* Uma variável que representa um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="cdf63-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdf63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdf63-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdf63-109">Nome</span><span class="sxs-lookup"><span data-stu-id="cdf63-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cdf63-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="cdf63-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cdf63-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cdf63-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cdf63-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdf63-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf63-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="cdf63-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="cdf63-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="cdf63-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="cdf63-115"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="cdf63-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf63-116">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdf63-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="cdf63-117">Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdf63-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf63-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="cdf63-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="cdf63-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="cdf63-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="cdf63-120"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="cdf63-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf63-121">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdf63-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="cdf63-122">Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="cdf63-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf63-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="cdf63-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="cdf63-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="cdf63-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="cdf63-125"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="cdf63-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf63-126">Um <strong>Variant</strong> que contém o valor inicial da propriedade.</span><span class="sxs-lookup"><span data-stu-id="cdf63-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="cdf63-127">Consulte a <strong><a href="field-value-property-dao.md">propriedade Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="cdf63-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf63-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="cdf63-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="cdf63-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="cdf63-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="cdf63-130"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="cdf63-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf63-131">Um <strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica se <strong>Property</strong> é ou não um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="cdf63-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="cdf63-132">O padrão é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdf63-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="cdf63-133">Se DDL for <strong>True</strong>, os usuários não poderão alterar ou excluir esse objeto <strong>Property,</strong> a menos que tenham <strong>permissão dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="cdf63-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="cdf63-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cdf63-134">Return value</span></span>

<span data-ttu-id="cdf63-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cdf63-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf63-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdf63-136">Remarks</span></span>

<span data-ttu-id="cdf63-137">Você pode criar um objeto **Property** definido pelo usuário na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="cdf63-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="cdf63-p105">Se você omitir uma ou mais das partes opcionais ao utilizar **CreateProperty**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas, as configurações de propriedade. Consulte os tópicos de propriedade **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="cdf63-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="cdf63-141">Se o nome se referir a um objeto que já é membro da coleção, ocorrerá um erro em tempo de executar quando você usar o **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="cdf63-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="cdf63-142">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **[Properties](properties-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="cdf63-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection.</span></span> <span data-ttu-id="cdf63-143">Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="cdf63-143">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="cdf63-144">Se você omitir o argumento DDL, ele será o padrão para False (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="cdf63-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="cdf63-145">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e criar um objeto **Property** que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="cdf63-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


