---
title: ExecuteOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8fa81d535a10aa0f359ba6e03b0f47048713671f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867850"
---
# <a name="executeoptionenum"></a><span data-ttu-id="ee293-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="ee293-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="ee293-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee293-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee293-104">Especifica como um provedor deve executar um comando.</span><span class="sxs-lookup"><span data-stu-id="ee293-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee293-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ee293-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee293-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ee293-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ee293-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee293-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee293-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-109">0x10</span><span class="sxs-lookup"><span data-stu-id="ee293-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="ee293-110">Indica que o comando deve ser executado de forma assíncrona .
</span><span class="sxs-lookup"><span data-stu-id="ee293-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="ee293-111">Este valor não pode ser combinado ao valor <a href="commandtypeenum.md">CommandTypeEnum </a><strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee293-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee293-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-113">0x20</span><span class="sxs-lookup"><span data-stu-id="ee293-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="ee293-114">Indica que as linhas restantes após a quantidade inicial especificada na propriedade <a href="cachesize-property-ado.md">CacheSize</a> devem ser recuperadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ee293-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee293-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-116">0x40</span><span class="sxs-lookup"><span data-stu-id="ee293-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="ee293-p102">Indica que um encadeamento principal nunca é bloqueado durante a recuperação. Se a linha solicitada não tiver sido recuperada, a linha atual se moverá automaticamente para o final do arquivo.
</span><span class="sxs-lookup"><span data-stu-id="ee293-p102">Indicates that the main thread never blocks while retrieving. If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="ee293-119">Se você abrir um <a href="recordset-object-ado.md">Recordset</a> a partir de um <a href="stream-object-ado.md">Stream</a> que contenha um <strong>Recordset</strong> persistentemente armazenado, <strong>adAsyncFetchNonBlocking</strong> não terá um efeito; a operação será síncrona e de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ee293-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="ee293-120">O <strong>adAsynchFetchNonBlocking</strong> não terá efeito quando a opção <a href="commandtypeenum.md">adCmdTableDirect</a> for usada para abrir o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee293-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee293-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-122">0x80</span><span class="sxs-lookup"><span data-stu-id="ee293-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="ee293-123">Indica que o texto do comando é um comando ou procedimento armazenado que não retorne linhas (por exemplo, um comando que apenas insere dados).</span><span class="sxs-lookup"><span data-stu-id="ee293-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="ee293-124">Se qualquer linha será recuperada, elas são descartadas e não retornadas.</span><span class="sxs-lookup"><span data-stu-id="ee293-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="ee293-125"><strong>adExecuteNoRecords</strong> pode ser transmitido como um parâmetro opcional para o <strong>comando</strong> ou o método <strong>Execute</strong> de <strong>Conexão</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee293-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee293-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-127">0x400</span><span class="sxs-lookup"><span data-stu-id="ee293-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="ee293-128">Indica que os resultados de uma execução de comando devem ser retornados como um fluxo.
</span><span class="sxs-lookup"><span data-stu-id="ee293-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="ee293-129"><strong>adExecuteStream</strong> pode ser transmitido como um parâmetro opcional para o método de <strong>execução</strong> do <strong>comando</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee293-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee293-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="ee293-131">Indica que o <strong>CommandText</strong> é um comando ou procedimento armazenado que retorna uma única linha que deve ser retornada como um objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee293-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee293-132"><strong>Feita</strong></span><span class="sxs-lookup"><span data-stu-id="ee293-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="ee293-133">-1</span><span class="sxs-lookup"><span data-stu-id="ee293-133">-1</span></span></p></td>
<td><p><span data-ttu-id="ee293-134">Indica que o comando não está especificado.</span><span class="sxs-lookup"><span data-stu-id="ee293-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ee293-135">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ee293-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="ee293-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ee293-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee293-137">Constante</span><span class="sxs-lookup"><span data-stu-id="ee293-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee293-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="ee293-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee293-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="ee293-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee293-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="ee293-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee293-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="ee293-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee293-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="ee293-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

