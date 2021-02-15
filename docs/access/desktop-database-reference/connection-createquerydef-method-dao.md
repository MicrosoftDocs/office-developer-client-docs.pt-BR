---
title: Método Connection.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295930"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="b9fbe-102">Método Connection.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9fbe-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="b9fbe-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9fbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9fbe-104">Crie um novo objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9fbe-105">Syntax</span></span>

<span data-ttu-id="b9fbe-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="b9fbe-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="b9fbe-107">*expressão* Uma variável que representa um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9fbe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9fbe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9fbe-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b9fbe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b9fbe-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="b9fbe-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b9fbe-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b9fbe-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b9fbe-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9fbe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9fbe-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b9fbe-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b9fbe-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="b9fbe-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9fbe-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9fbe-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9fbe-116">Um <strong>Variant</strong> (<strong>String</strong> subtype) que exclusivamente nomeia a nova <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9fbe-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="b9fbe-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="b9fbe-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="b9fbe-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9fbe-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9fbe-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9fbe-120">Um <strong>Variant</strong> (<strong>String</strong> subtype) que é uma instrução SQL definindo o <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="b9fbe-121">Se você omitir esse argumento, será possível definir o <strong>QueryDef</strong> configurando sua propriedade <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes ou depois de acrescentá-lo a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b9fbe-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b9fbe-122">Return value</span></span>

<span data-ttu-id="b9fbe-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="b9fbe-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="b9fbe-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9fbe-124">Remarks</span></span>

<span data-ttu-id="b9fbe-125">Em um espaço de trabalho do Microsoft Access, se você fornecer algo diferente de uma cadeia de caracteres de comprimento zero para o nome ao criar um **QueryDef**, o objeto **QueryDef** resultante será automaticamente acrescentado à coleção **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="b9fbe-126">Se o objeto especificado por name já for um membro da coleção **QueryDefs**, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="b9fbe-127">Você pode criar um **QueryDef** temporário usando uma cadeia de caracteres de comprimento zero para o argumento name quando executar o método **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="b9fbe-128">Também é possível realizar isso configurando a propriedade **[Name](connection-name-property-dao.md)** de um **QueryDef** recém-criado como uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="b9fbe-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="b9fbe-129">Objetos **QueryDef** temporários são úteis se você desejar usar repetidamente instruções SQL dinâmicas sem ter de criar novos objetos permanentes na coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="b9fbe-130">Não é possível acrescentar um **QueryDef** temporário a qualquer coleção porque uma cadeia de caracteres de comprimento zero não é um nome válido para um objeto **QueryDef** permanente.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="b9fbe-131">Sempre é possível definir as propriedades **Name** e **SQL** do objeto **QueryDef** recém-criado e subsequentemente acrescentar o **QueryDef** à coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="b9fbe-132">Para executar a instrução SQL em um objeto **QueryDef**, use o método **[Execute](connection-execute-method-dao.md)** ou **[OpenRecordset](connection-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="b9fbe-133">Usar um objeto **QueryDef** é a maneira preferencial de executar consultas passagem SQL com bancos de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="b9fbe-134">Para remover um objeto **QueryDef** de uma coleção **QueryDefs** em um banco de dados de mecanismo de banco de dados Microsoft Access, use o método **[Delete](fields-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="b9fbe-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

