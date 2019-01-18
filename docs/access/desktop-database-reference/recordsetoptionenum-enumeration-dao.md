---
title: Enumeração RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717276"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="10974-102">Enumeração RecordsetOptionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="10974-102">RecordsetOptionEnum enumeration (DAO)</span></span>


<span data-ttu-id="10974-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="10974-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10974-104">Usada com o método **OpenRecordset** para especificar as características de um novo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="10974-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10974-105">Nome</span><span class="sxs-lookup"><span data-stu-id="10974-105">Name</span></span></p></th>
<th><p><span data-ttu-id="10974-106">Valor</span><span class="sxs-lookup"><span data-stu-id="10974-106">Value</span></span></p></th>
<th><p><span data-ttu-id="10974-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="10974-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10974-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="10974-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="10974-109">8</span><span class="sxs-lookup"><span data-stu-id="10974-109">8</span></span></p></td>
<td><p><span data-ttu-id="10974-110">Permite ao usuário adicionar novos registros ao dynaset, mas impede que ele leia registros existentes.</span><span class="sxs-lookup"><span data-stu-id="10974-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="10974-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="10974-112">32</span><span class="sxs-lookup"><span data-stu-id="10974-112">32</span></span></p></td>
<td><p><span data-ttu-id="10974-113">Aplica atualizações somente aos campos que não irão afetar outros registros do dynaset (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="10974-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10974-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="10974-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="10974-115">2</span><span class="sxs-lookup"><span data-stu-id="10974-115">2</span></span></p></td>
<td><p><span data-ttu-id="10974-116">Impede que outros usuários leiam registros do conjunto de registros (somente tipo tabela).</span><span class="sxs-lookup"><span data-stu-id="10974-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="10974-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="10974-118">1</span><span class="sxs-lookup"><span data-stu-id="10974-118">1</span></span></p></td>
<td><p><span data-ttu-id="10974-119">Impede que outros usuários alterem registros do Conjunto de Registros.</span><span class="sxs-lookup"><span data-stu-id="10974-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10974-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="10974-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="10974-121">2048</span><span class="sxs-lookup"><span data-stu-id="10974-121">2048</span></span></p></td>
<td><p><span data-ttu-id="10974-122">Executa a consulta sem primeiro chamar a função SQLPrepare do ODBC.</span><span class="sxs-lookup"><span data-stu-id="10974-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="10974-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="10974-124">128</span><span class="sxs-lookup"><span data-stu-id="10974-124">128</span></span></p></td>
<td><p><span data-ttu-id="10974-125">Reverte as atualizações quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="10974-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10974-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="10974-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="10974-127">256</span><span class="sxs-lookup"><span data-stu-id="10974-127">256</span></span></p></td>
<td><p><span data-ttu-id="10974-128">Cria um Conjunto de Registros de rolagem, do tipo instantâneo, somente de encaminhamento (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="10974-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="10974-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="10974-130">16</span><span class="sxs-lookup"><span data-stu-id="10974-130">16</span></span></p></td>
<td><p><span data-ttu-id="10974-131">Aplica atualizações a todos os campos dynaset, mesmo que outros registros sejam afetados (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="10974-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10974-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="10974-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="10974-133">4</span><span class="sxs-lookup"><span data-stu-id="10974-133">4</span></span></p></td>
<td><p><span data-ttu-id="10974-134">Abre o Conjunto de Registros como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="10974-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="10974-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="10974-136">1024</span><span class="sxs-lookup"><span data-stu-id="10974-136">1024</span></span></p></td>
<td><p><span data-ttu-id="10974-137">Executa a consulta de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="10974-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10974-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="10974-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="10974-139">512</span><span class="sxs-lookup"><span data-stu-id="10974-139">512</span></span></p></td>
<td><p><span data-ttu-id="10974-140">Gera um erro em tempo de execução se outro usuário estiver alterando dados que você estiver editando (somente tipo dynaset).</span><span class="sxs-lookup"><span data-stu-id="10974-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10974-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="10974-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="10974-142">64</span><span class="sxs-lookup"><span data-stu-id="10974-142">64</span></span></p></td>
<td><p><span data-ttu-id="10974-143">Envia uma instrução SQL a um banco de dados ODBC (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="10974-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

