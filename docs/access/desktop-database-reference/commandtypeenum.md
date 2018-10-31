---
title: CommandTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cc5fee66746270f5ba8ee851010c6860cfc9e791
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861061"
---
# <a name="commandtypeenum"></a><span data-ttu-id="f8091-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f8091-102">CommandTypeEnum</span></span>

<span data-ttu-id="f8091-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8091-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8091-104">Especifica como um argumento de comando deve ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="f8091-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8091-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f8091-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f8091-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f8091-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f8091-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8091-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8091-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-109">-1</span><span class="sxs-lookup"><span data-stu-id="f8091-109">-1</span></span></p></td>
<td><p><span data-ttu-id="f8091-110">Não especifica o argumento de tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="f8091-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-112">1</span><span class="sxs-lookup"><span data-stu-id="f8091-112">1</span></span></p></td>
<td><p><span data-ttu-id="f8091-113">Avalia o <a href="commandtext-property-ado.md">CommandText</a> como uma definição textual de um comando ou chamada de procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="f8091-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-115">2</span><span class="sxs-lookup"><span data-stu-id="f8091-115">2</span></span></p></td>
<td><p><span data-ttu-id="f8091-116">Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas por uma consulta SQL gerada internamente.</span><span class="sxs-lookup"><span data-stu-id="f8091-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-118">4</span><span class="sxs-lookup"><span data-stu-id="f8091-118">4</span></span></p></td>
<td><p><span data-ttu-id="f8091-119">Avalia o <strong>CommandText</strong> como um nome de procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="f8091-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-121">8</span><span class="sxs-lookup"><span data-stu-id="f8091-121">8</span></span></p></td>
<td><p><span data-ttu-id="f8091-p101">Padrão. Indica que o tipo de comando na propriedade <strong>CommandText</strong> não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f8091-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-125">256</span><span class="sxs-lookup"><span data-stu-id="f8091-125">256</span></span></p></td>
<td><p><span data-ttu-id="f8091-p102">Avalia o <strong>CommandText</strong> como o nome do arquivo de um <a href="recordset-object-ado.md">Recordset</a> armazenado de forma persistente. Utilizado com <strong>Recordset.</strong>Apenas <a href="open-method-ado-recordset.md">Open</a> ou <a href="requery-method-ado.md">Requery</a>.</span><span class="sxs-lookup"><span data-stu-id="f8091-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="f8091-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="f8091-129">512</span><span class="sxs-lookup"><span data-stu-id="f8091-129">512</span></span></p></td>
<td><p><span data-ttu-id="f8091-130">Avalia o <strong>CommandText</strong> como um nome de tabela cujas colunas são todas retornadas.</span><span class="sxs-lookup"><span data-stu-id="f8091-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="f8091-131">Usado somente com <strong>Recordset</strong> ou <strong>Requery</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8091-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="f8091-132">Para usar o método <a href="seek-method-ado.md">Seek</a> , o <strong>Recordset</strong> deve ser aberto com <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8091-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="f8091-133">Esse valor não pode ser combinado com o valor  <strong>adAsyncExecute </strong><a href="executeoptionenum.md">ExecuteOptionEnum</a>.</span><span class="sxs-lookup"><span data-stu-id="f8091-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f8091-134">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f8091-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="f8091-135">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f8091-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8091-136">Constante</span><span class="sxs-lookup"><span data-stu-id="f8091-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8091-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="f8091-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="f8091-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="f8091-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="f8091-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="f8091-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8091-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="f8091-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8091-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="f8091-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

