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
ms.openlocfilehash: a03f486d29aa70c7d4901372f81609e378ffae07
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950052"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="45a3b-102">Método Connection.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="45a3b-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="45a3b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="45a3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45a3b-104">Cria um novo objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="45a3b-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45a3b-105">Syntax</span></span>

<span data-ttu-id="45a3b-106">*expressão* . CreateQueryDef (***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="45a3b-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="45a3b-107">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="45a3b-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="45a3b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45a3b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45a3b-109">Nome</span><span class="sxs-lookup"><span data-stu-id="45a3b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="45a3b-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="45a3b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="45a3b-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="45a3b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="45a3b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="45a3b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45a3b-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="45a3b-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="45a3b-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="45a3b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="45a3b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="45a3b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="45a3b-116">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="45a3b-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a3b-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="45a3b-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="45a3b-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="45a3b-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="45a3b-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="45a3b-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="45a3b-p101">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que é uma instrução SQL definindo o <strong>QueryDef</strong>. Se você omitir esse argumento, será possível definir o <strong>QueryDef</strong> configurando sua propriedade <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes ou depois de acrescentá-lo a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="45a3b-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="45a3b-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="45a3b-122">Return value</span></span>

<span data-ttu-id="45a3b-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="45a3b-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="45a3b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="45a3b-124">Remarks</span></span>

<span data-ttu-id="45a3b-125">Em um espaço de trabalho do Microsoft Access, se você fornecer algo diferente de uma cadeia de caracteres de comprimento zero para o nome ao criar um **QueryDef**, o objeto **QueryDef** resultante será automaticamente acrescentado à coleção **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="45a3b-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="45a3b-126">Se o objeto especificado pelo nome, já é um membro da coleção **QueryDefs** , ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="45a3b-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="45a3b-127">Você pode criar um temporário **QueryDef** usando uma cadeia de caracteres de comprimento zero para o argumento nome quando você executar o método **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="45a3b-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="45a3b-128">Também é possível realizar isso configurando a propriedade **[Name](connection-name-property-dao.md)** de um **QueryDef** recém-criado como uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="45a3b-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="45a3b-129">Objetos **QueryDef** temporários são úteis se você desejar usar repetidamente instruções SQL dinâmicas sem ter de criar novos objetos permanentes na coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="45a3b-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="45a3b-130">Não é possível acrescentar um **QueryDef** temporário a qualquer coleção porque uma cadeia de caracteres de comprimento zero não é um nome válido para um objeto **QueryDef** permanente.</span><span class="sxs-lookup"><span data-stu-id="45a3b-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="45a3b-131">Sempre é possível definir as propriedades **Name** e **SQL** do objeto **QueryDef** recém-criado e subsequentemente acrescentar o **QueryDef** à coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="45a3b-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="45a3b-132">Para executar a instrução SQL em um objeto **QueryDef**, use o método **[Execute](connection-execute-method-dao.md)** ou **[OpenRecordset](connection-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="45a3b-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="45a3b-133">Usar um objeto **QueryDef** é a maneira preferencial de executar consultas passagem SQL com bancos de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="45a3b-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="45a3b-134">Para remover um objeto **QueryDef** de uma coleção **QueryDefs** em um banco de dados de mecanismo de banco de dados Microsoft Access, use o método **[Delete](fields-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="45a3b-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

