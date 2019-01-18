---
title: CommandTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714273"
---
# <a name="commandtypeenum"></a><span data-ttu-id="849b6-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="849b6-102">CommandTypeEnum</span></span>

<span data-ttu-id="849b6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="849b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="849b6-104">Especifica como um argumento de comando deve ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="849b6-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="849b6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="849b6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="849b6-106">Valor</span><span class="sxs-lookup"><span data-stu-id="849b6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="849b6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="849b6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="849b6-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-109">-1</span><span class="sxs-lookup"><span data-stu-id="849b6-109">-1</span></span></p></td>
<td><p><span data-ttu-id="849b6-110">Não especifica o argumento de tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="849b6-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-112">1</span><span class="sxs-lookup"><span data-stu-id="849b6-112">1</span></span></p></td>
<td><p><span data-ttu-id="849b6-113">Avalia o <a href="commandtext-property-ado.md">CommandText</a> como uma definição textual de um comando ou chamada de procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="849b6-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-115">2</span><span class="sxs-lookup"><span data-stu-id="849b6-115">2</span></span></p></td>
<td><p><span data-ttu-id="849b6-116">Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas por uma consulta SQL gerada internamente.</span><span class="sxs-lookup"><span data-stu-id="849b6-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-118">4</span><span class="sxs-lookup"><span data-stu-id="849b6-118">4</span></span></p></td>
<td><p><span data-ttu-id="849b6-119">Avalia o <strong>CommandText</strong> como um nome de procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="849b6-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-121">8</span><span class="sxs-lookup"><span data-stu-id="849b6-121">8</span></span></p></td>
<td><p><span data-ttu-id="849b6-p101">Padrão. Indica que o tipo de comando na propriedade <strong>CommandText</strong> não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="849b6-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-125">256</span><span class="sxs-lookup"><span data-stu-id="849b6-125">256</span></span></p></td>
<td><p><span data-ttu-id="849b6-p102">Avalia o <strong>CommandText</strong> como o nome do arquivo de um <a href="recordset-object-ado.md">Recordset</a> armazenado de forma persistente. Utilizado com <strong>Recordset.</strong>Apenas <a href="open-method-ado-recordset.md">Open</a> ou <a href="requery-method-ado.md">Requery</a>.</span><span class="sxs-lookup"><span data-stu-id="849b6-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="849b6-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="849b6-129">512</span><span class="sxs-lookup"><span data-stu-id="849b6-129">512</span></span></p></td>
<td><p><span data-ttu-id="849b6-130">Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas.</span><span class="sxs-lookup"><span data-stu-id="849b6-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="849b6-131">Usado somente com <strong>Recordset</strong> ou <strong>Requery</strong> .</span><span class="sxs-lookup"><span data-stu-id="849b6-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="849b6-132">Para usar o método <a href="seek-method-ado.md">Seek</a> , o <strong>Recordset</strong> deve ser aberto com <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="849b6-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="849b6-133">Esse valor não pode ser combinado com o valor  <strong>adAsyncExecute </strong><a href="executeoptionenum.md">ExecuteOptionEnum</a>.</span><span class="sxs-lookup"><span data-stu-id="849b6-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="849b6-134">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="849b6-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="849b6-135">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="849b6-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="849b6-136">Constante</span><span class="sxs-lookup"><span data-stu-id="849b6-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="849b6-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="849b6-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="849b6-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="849b6-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="849b6-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="849b6-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849b6-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="849b6-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="849b6-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="849b6-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

