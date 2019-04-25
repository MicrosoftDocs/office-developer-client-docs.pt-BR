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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307179"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="5ecdc-102">Enumeração RecordsetOptionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="5ecdc-102">RecordsetOptionEnum enumeration (DAO)</span></span>


<span data-ttu-id="5ecdc-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ecdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ecdc-104">Usado com o método **OpenRecordset** para especificar as características de um novo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ecdc-105">Nome</span><span class="sxs-lookup"><span data-stu-id="5ecdc-105">Name</span></span></p></th>
<th><p><span data-ttu-id="5ecdc-106">Valor</span><span class="sxs-lookup"><span data-stu-id="5ecdc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5ecdc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ecdc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="5ecdc-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-109">8</span><span class="sxs-lookup"><span data-stu-id="5ecdc-109">8.</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-110">Permite ao usuário adicionar novos registros ao dynaset, mas impede que ele leia registros existentes.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="5ecdc-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-112">32</span><span class="sxs-lookup"><span data-stu-id="5ecdc-112">3.2</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-113">Aplica atualizações somente aos campos que não irão afetar outros registros do dynaset (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="5ecdc-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-115">2</span><span class="sxs-lookup"><span data-stu-id="5ecdc-115">2.</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-116">Impede que outros usuários leiam registros do Conjunto de Registros (somente tipo tabela).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-116">Prevents other users from reading Recordset records (table-type  only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="5ecdc-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-118">1</span><span class="sxs-lookup"><span data-stu-id="5ecdc-118">-1</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-119">Impede que outros usuários alterem registros do Conjunto de Registros.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="5ecdc-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-121">2048</span><span class="sxs-lookup"><span data-stu-id="5ecdc-121">2048 MB</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-122">Executa a consulta sem primeiro chamar a função SQLPrepare do ODBC.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="5ecdc-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-124">128</span><span class="sxs-lookup"><span data-stu-id="5ecdc-124">128 bits</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-125">Reverte as atualizações quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="5ecdc-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-127">256</span><span class="sxs-lookup"><span data-stu-id="5ecdc-127">validAccesses: 256</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-128">Cria um Conjunto de Registros de rolagem, do tipo instantâneo, somente de encaminhamento (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="5ecdc-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-130">16</span><span class="sxs-lookup"><span data-stu-id="5ecdc-130">1.6</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-131">Aplica atualizações a todos os campos dynaset, mesmo que outros registros sejam afetados (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="5ecdc-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-133">4</span><span class="sxs-lookup"><span data-stu-id="5ecdc-133">4.</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-134">Abre o Conjunto de Registros como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="5ecdc-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-136">1024</span><span class="sxs-lookup"><span data-stu-id="5ecdc-136">1024 attachments4</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-137">Executa a consulta de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5ecdc-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ecdc-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="5ecdc-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-139">512</span><span class="sxs-lookup"><span data-stu-id="5ecdc-139">5.12</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-140">Gera um erro em tempo de execução se outro usuário estiver alterando dados que você estiver editando (somente tipo dynaset).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ecdc-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="5ecdc-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-142">64</span><span class="sxs-lookup"><span data-stu-id="5ecdc-142">6.4</span></span></p></td>
<td><p><span data-ttu-id="5ecdc-143">Envia uma instrução SQL a um banco de dados ODBC (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="5ecdc-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

