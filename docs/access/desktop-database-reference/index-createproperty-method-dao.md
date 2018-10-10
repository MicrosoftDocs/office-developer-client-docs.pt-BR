---
title: Método Index.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 712bccd2-c8a8-cc96-6f77-6d93d92320d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195775(v=office.15)
ms:contentKeyID: 48545578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 47b7619123e9fd0761ff14f7938ae2bfe99f9b8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463486"
---
# <a name="indexcreateproperty-method-dao"></a><span data-ttu-id="25eb5-102">Método Index.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="25eb5-102">Index.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="25eb5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="25eb5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="25eb5-104">Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25eb5-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="25eb5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25eb5-105">Syntax</span></span>

<span data-ttu-id="25eb5-106">*expressão* . CreateProperty (***nome***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="25eb5-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="25eb5-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="25eb5-107">*expression* A variable that represents an **Index** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="25eb5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25eb5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25eb5-109">Nome</span><span class="sxs-lookup"><span data-stu-id="25eb5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="25eb5-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="25eb5-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="25eb5-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="25eb5-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="25eb5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="25eb5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25eb5-113">Name</span><span class="sxs-lookup"><span data-stu-id="25eb5-113">Name</span></span></p></td>
<td><p><span data-ttu-id="25eb5-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="25eb5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="25eb5-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="25eb5-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="25eb5-p101">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="25eb5-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25eb5-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="25eb5-118">Type</span></span></p></td>
<td><p><span data-ttu-id="25eb5-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="25eb5-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="25eb5-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="25eb5-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="25eb5-p102">Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="25eb5-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25eb5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="25eb5-123">Value</span></span></p></td>
<td><p><span data-ttu-id="25eb5-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="25eb5-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="25eb5-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="25eb5-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="25eb5-p103">Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="25eb5-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25eb5-128">DDL</span><span class="sxs-lookup"><span data-stu-id="25eb5-128">DDL</span></span></p></td>
<td><p><span data-ttu-id="25eb5-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="25eb5-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="25eb5-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="25eb5-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="25eb5-131">Um <strong>Variant</strong> (subtipo<strong>booleano</strong> ) que indica se é ou não a <strong>propriedade</strong> de um objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="25eb5-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="25eb5-132">O padrão é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="25eb5-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="25eb5-133">Se DDL for <strong>True</strong>, os usuários não podem alterar ou excluir esse objeto de <strong>propriedade</strong> , a menos que tenham permissão <strong>dbSecWriteDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="25eb5-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="25eb5-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="25eb5-134">Return Value</span></span>

<span data-ttu-id="25eb5-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="25eb5-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="25eb5-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="25eb5-136">Remarks</span></span>

<span data-ttu-id="25eb5-137">Você pode criar um objeto **Property** definido pelo usuário somente na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.</span><span class="sxs-lookup"><span data-stu-id="25eb5-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="25eb5-p105">Se omitir uma ou mais dessas partes opcionais quando usar **CreateProperty**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos de propriedade de **Name**, **Type** e **Value** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="25eb5-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="25eb5-141">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="25eb5-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="25eb5-p106">Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**. Não é possível excluir propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="25eb5-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="25eb5-144">Se você omitir o argumento DDL, o padrão é False (não-DDL).</span><span class="sxs-lookup"><span data-stu-id="25eb5-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="25eb5-145">Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar um objeto <STRONG>Property</STRONG> que deseja alterar de DDL para não-DDL.</span><span class="sxs-lookup"><span data-stu-id="25eb5-145">Because no corresponding DDL property is exposed, you must delete and re-create a <STRONG>Property</STRONG> object you want to change from DDL to non-DDL.</span></span></P>


