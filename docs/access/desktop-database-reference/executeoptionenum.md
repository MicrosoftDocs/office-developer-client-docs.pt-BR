---
title: ExecuteOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aeb1083c693e0848e30a0b9217ae709994daddb5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463503"
---
# <a name="executeoptionenum"></a><span data-ttu-id="9d7b3-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="9d7b3-102">ExecuteOptionEnum</span></span>


<span data-ttu-id="9d7b3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d7b3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9d7b3-104">Especifica como um provedor deve executar um comando.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-104">Specifies how a provider should execute a command.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d7b3-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9d7b3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9d7b3-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9d7b3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9d7b3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d7b3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-109">0x10</span><span class="sxs-lookup"><span data-stu-id="9d7b3-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-110">Indica que o comando deve ser executado de forma assíncrona .
</span><span class="sxs-lookup"><span data-stu-id="9d7b3-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="9d7b3-111">Este valor não pode ser combinado ao valor <a href="commandtypeenum.md">CommandTypeEnum </a><strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d7b3-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-113">0x20</span><span class="sxs-lookup"><span data-stu-id="9d7b3-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-114">Indica que as linhas restantes após a quantidade inicial especificada na propriedade <a href="cachesize-property-ado.md">CacheSize</a> devem ser recuperadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-116">0x40</span><span class="sxs-lookup"><span data-stu-id="9d7b3-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-117">Indica que o thread principal nunca bloqueia ao recuperar.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-117">Indicates that the main thread never blocks while retrieving.</span></span> <span data-ttu-id="9d7b3-118">Se a linha solicitada não foi recuperada, a linha atual se move automaticamente até o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-118">If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span> <span data-ttu-id="9d7b3-119">Se você abrir um <a href="recordset-object-ado.md">Recordset</a> a partir de um <a href="stream-object-ado.md">Stream</a> que contenha um <strong>Recordset</strong> persistentemente armazenado, <strong>adAsyncFetchNonBlocking</strong> não terá um efeito; a operação será síncrona e de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="9d7b3-120">O <strong>adAsynchFetchNonBlocking</strong> não terá efeito quando a opção <a href="commandtypeenum.md">adCmdTableDirect</a> for usada para abrir o <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d7b3-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-122">0x80</span><span class="sxs-lookup"><span data-stu-id="9d7b3-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-123">Indica que o texto do comando é um comando ou procedimento armazenado que não retorne linhas (por exemplo, um comando que apenas insere dados).</span><span class="sxs-lookup"><span data-stu-id="9d7b3-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="9d7b3-124">Se qualquer linha será recuperada, elas são descartadas e não retornadas.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="9d7b3-125"><strong>adExecuteNoRecords</strong> pode ser transmitido como um parâmetro opcional para o <strong>comando</strong> ou o método <strong>Execute</strong> de <strong>Conexão</strong> .</span><span class="sxs-lookup"><span data-stu-id="9d7b3-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-127">0x400</span><span class="sxs-lookup"><span data-stu-id="9d7b3-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-128">Indica que os resultados de uma execução de comando devem ser retornados como um fluxo.
</span><span class="sxs-lookup"><span data-stu-id="9d7b3-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="9d7b3-129"><strong>adExecuteStream</strong> pode ser transmitido como um parâmetro opcional para o método de <strong>execução</strong> do <strong>comando</strong> .</span><span class="sxs-lookup"><span data-stu-id="9d7b3-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d7b3-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="9d7b3-131">Indica que o <strong>CommandText</strong> é um comando ou procedimento armazenado que retorna uma única linha que deve ser retornada como um objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-132"><strong>Feita</strong></span><span class="sxs-lookup"><span data-stu-id="9d7b3-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9d7b3-133">-1</span><span class="sxs-lookup"><span data-stu-id="9d7b3-133">-1</span></span></p></td>
<td><p><span data-ttu-id="9d7b3-134">Indica que o comando não está especificado.</span><span class="sxs-lookup"><span data-stu-id="9d7b3-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d7b3-135">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="9d7b3-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="9d7b3-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9d7b3-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d7b3-137">Constante</span><span class="sxs-lookup"><span data-stu-id="9d7b3-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="9d7b3-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d7b3-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="9d7b3-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="9d7b3-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d7b3-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="9d7b3-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d7b3-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9d7b3-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

