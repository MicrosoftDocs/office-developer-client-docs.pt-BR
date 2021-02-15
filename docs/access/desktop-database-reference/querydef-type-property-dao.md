---
title: Propriedade QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300942"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="9aa2e-102">Propriedade QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="9aa2e-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="9aa2e-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aa2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aa2e-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="9aa2e-105">Somente leitura **inteiro**.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa2e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa2e-106">Syntax</span></span>

<span data-ttu-id="9aa2e-107">*expressão* .Type</span><span class="sxs-lookup"><span data-stu-id="9aa2e-107">*expression* .Type</span></span>

<span data-ttu-id="9aa2e-108">*expressão* Uma variável que representa um objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa2e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa2e-109">Remarks</span></span>

<span data-ttu-id="9aa2e-110">Para um objeto **QueryDef**, as configurações e os valores de retorno possíveis são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9aa2e-111">Constant</span><span class="sxs-lookup"><span data-stu-id="9aa2e-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="9aa2e-112">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="9aa2e-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-114">Ação</span><span class="sxs-lookup"><span data-stu-id="9aa2e-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-116">Append</span><span class="sxs-lookup"><span data-stu-id="9aa2e-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-118">Composto</span><span class="sxs-lookup"><span data-stu-id="9aa2e-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-120">Crosstab</span><span class="sxs-lookup"><span data-stu-id="9aa2e-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-122">Definição de dados</span><span class="sxs-lookup"><span data-stu-id="9aa2e-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-124">Excluir</span><span class="sxs-lookup"><span data-stu-id="9aa2e-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-126">Make-table</span><span class="sxs-lookup"><span data-stu-id="9aa2e-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-128">Procedimento (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="9aa2e-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="9aa2e-129"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9aa2e-130">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-132">Selecionar</span><span class="sxs-lookup"><span data-stu-id="9aa2e-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-134">União</span><span class="sxs-lookup"><span data-stu-id="9aa2e-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-136">Usado com <strong>dbQSQLPassThrough</strong> para especificar um consulta que não retorna registros (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9aa2e-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aa2e-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-138">Passagem (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="9aa2e-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aa2e-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="9aa2e-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="9aa2e-140">Atualizar</span><span class="sxs-lookup"><span data-stu-id="9aa2e-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9aa2e-141">Quando você acrescentar um novo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** ou **[Property](property-object-dao.md)** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

