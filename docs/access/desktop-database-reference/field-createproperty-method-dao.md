---
title: Método Field.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71d5a77543de05cd440e5b5c2cf40596d141b16d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926147"
---
# <a name="fieldcreateproperty-method-dao"></a><span data-ttu-id="31cef-102">Método Field.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="31cef-102">Field.CreateProperty method (DAO)</span></span>


<span data-ttu-id="31cef-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="31cef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31cef-104">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31cef-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="31cef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31cef-105">Syntax</span></span>

<span data-ttu-id="31cef-106">*expressão* . CreateProperty (***nome***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="31cef-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="31cef-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="31cef-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="31cef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31cef-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31cef-109">Nome</span><span class="sxs-lookup"><span data-stu-id="31cef-109">Name</span></span></p></th>
<th><p><span data-ttu-id="31cef-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="31cef-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="31cef-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="31cef-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="31cef-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="31cef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31cef-113">Name</span><span class="sxs-lookup"><span data-stu-id="31cef-113">Name</span></span></p></td>
<td><p><span data-ttu-id="31cef-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="31cef-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="31cef-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="31cef-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="31cef-p101">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="31cef-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31cef-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="31cef-118">Type</span></span></p></td>
<td><p><span data-ttu-id="31cef-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="31cef-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="31cef-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="31cef-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="31cef-p102">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="31cef-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31cef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31cef-123">Value</span></span></p></td>
<td><p><span data-ttu-id="31cef-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="31cef-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="31cef-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="31cef-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="31cef-p103">Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="31cef-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31cef-128">DDL</span><span class="sxs-lookup"><span data-stu-id="31cef-128">DDL</span></span></p></td>
<td><p><span data-ttu-id="31cef-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="31cef-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="31cef-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="31cef-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="31cef-131">Um <strong>Variant</strong> (subtipo<strong>booleano</strong> ) que indica se é ou não a <strong>propriedade</strong> de um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="31cef-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="31cef-132">O padrão é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="31cef-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="31cef-133">Se DDL for <strong>True</strong>, os usuários não podem alterar ou excluir esse objeto de <strong>propriedade</strong> , a menos que tenham permissão <strong>dbSecWriteDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="31cef-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="31cef-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="31cef-134">Return value</span></span>

<span data-ttu-id="31cef-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="31cef-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="31cef-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="31cef-136">Remarks</span></span>

<span data-ttu-id="31cef-137">Você pode criar um objeto **Property** definido pelo usuário somente na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="31cef-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="31cef-p105">Se omitir uma ou mais dessas partes opcionais quando usar **CreateProperty**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos de propriedade de **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="31cef-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="31cef-141">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="31cef-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="31cef-p106">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**. Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="31cef-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="31cef-144">Se você omitir o argumento DDL, o padrão é False (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="31cef-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="31cef-145">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar um objeto **Property** que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="31cef-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


