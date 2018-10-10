---
title: Enumeração RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462419"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="dec6a-102">Enumeração RecordsetOptionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="dec6a-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="dec6a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dec6a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dec6a-104">Usada com o método **OpenRecordset** para especificar as características de um novo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="dec6a-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dec6a-105">Nome</span><span class="sxs-lookup"><span data-stu-id="dec6a-105">Name</span></span></p></th>
<th><p><span data-ttu-id="dec6a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="dec6a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dec6a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dec6a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="dec6a-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="dec6a-109">8</span><span class="sxs-lookup"><span data-stu-id="dec6a-109">8</span></span></p></td>
<td><p><span data-ttu-id="dec6a-110">Permite ao usuário adicionar novos registros ao dynaset, mas impede que ele leia registros existentes.</span><span class="sxs-lookup"><span data-stu-id="dec6a-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="dec6a-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="dec6a-112">32</span><span class="sxs-lookup"><span data-stu-id="dec6a-112">32</span></span></p></td>
<td><p><span data-ttu-id="dec6a-113">Aplica atualizações somente aos campos que não irão afetar outros registros do dynaset (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="dec6a-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="dec6a-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="dec6a-115">2</span><span class="sxs-lookup"><span data-stu-id="dec6a-115">2</span></span></p></td>
<td><p><span data-ttu-id="dec6a-116">Impede que outros usuários leiam registros do conjunto de registros (somente tipo tabela).</span><span class="sxs-lookup"><span data-stu-id="dec6a-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="dec6a-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="dec6a-118">1</span><span class="sxs-lookup"><span data-stu-id="dec6a-118">1</span></span></p></td>
<td><p><span data-ttu-id="dec6a-119">Impede que outros usuários alterem registros do Conjunto de Registros.</span><span class="sxs-lookup"><span data-stu-id="dec6a-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="dec6a-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="dec6a-121">2048</span><span class="sxs-lookup"><span data-stu-id="dec6a-121">2048</span></span></p></td>
<td><p><span data-ttu-id="dec6a-122">Executa a consulta sem primeiro chamar a função SQLPrepare do ODBC.</span><span class="sxs-lookup"><span data-stu-id="dec6a-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="dec6a-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="dec6a-124">128</span><span class="sxs-lookup"><span data-stu-id="dec6a-124">128</span></span></p></td>
<td><p><span data-ttu-id="dec6a-125">Reverte as atualizações quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="dec6a-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="dec6a-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="dec6a-127">256</span><span class="sxs-lookup"><span data-stu-id="dec6a-127">256</span></span></p></td>
<td><p><span data-ttu-id="dec6a-128">Cria um Conjunto de Registros de rolagem, do tipo instantâneo, somente de encaminhamento (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="dec6a-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="dec6a-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="dec6a-130">16</span><span class="sxs-lookup"><span data-stu-id="dec6a-130">16</span></span></p></td>
<td><p><span data-ttu-id="dec6a-131">Aplica atualizações a todos os campos dynaset, mesmo que outros registros sejam afetados (somente tipos dynaset e instantâneo).</span><span class="sxs-lookup"><span data-stu-id="dec6a-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="dec6a-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="dec6a-133">4</span><span class="sxs-lookup"><span data-stu-id="dec6a-133">4</span></span></p></td>
<td><p><span data-ttu-id="dec6a-134">Abre o Conjunto de Registros como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="dec6a-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="dec6a-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="dec6a-136">1024</span><span class="sxs-lookup"><span data-stu-id="dec6a-136">1024</span></span></p></td>
<td><p><span data-ttu-id="dec6a-137">Executa a consulta de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="dec6a-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec6a-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="dec6a-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="dec6a-139">512</span><span class="sxs-lookup"><span data-stu-id="dec6a-139">512</span></span></p></td>
<td><p><span data-ttu-id="dec6a-140">Gera um erro em tempo de execução se outro usuário estiver alterando dados que você estiver editando (somente tipo dynaset).</span><span class="sxs-lookup"><span data-stu-id="dec6a-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec6a-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="dec6a-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="dec6a-142">64</span><span class="sxs-lookup"><span data-stu-id="dec6a-142">64</span></span></p></td>
<td><p><span data-ttu-id="dec6a-143">Envia uma instrução SQL a um banco de dados ODBC (somente tipo instantâneo).</span><span class="sxs-lookup"><span data-stu-id="dec6a-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

