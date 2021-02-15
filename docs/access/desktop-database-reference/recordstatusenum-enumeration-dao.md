---
title: Enumeração RecordStatusEnum (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb7bffaf91db9e1170702d2e36393da669dbe0c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309231"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="b0715-102">Enumeração RecordStatusEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0715-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="b0715-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0715-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0715-104">Usada com a propriedade **RecordStatus** para indicar o status de atualização do registro atual, se ele fizer parte de uma atualização em lotes.</span><span class="sxs-lookup"><span data-stu-id="b0715-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0715-105">Nome</span><span class="sxs-lookup"><span data-stu-id="b0715-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b0715-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b0715-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b0715-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0715-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0715-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="b0715-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="b0715-109">4 </span><span class="sxs-lookup"><span data-stu-id="b0715-109">4</span></span></p></td>
<td><p><span data-ttu-id="b0715-110">O registro foi excluído localmente e no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0715-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0715-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="b0715-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="b0715-112">3 </span><span class="sxs-lookup"><span data-stu-id="b0715-112">3</span></span></p></td>
<td><p><span data-ttu-id="b0715-113">O registro foi excluído, mas ainda não foi excluído do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0715-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0715-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="b0715-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="b0715-115">1 </span><span class="sxs-lookup"><span data-stu-id="b0715-115">1</span></span></p></td>
<td><p><span data-ttu-id="b0715-116">O registro foi modificado e não foi atualizado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0715-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0715-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="b0715-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="b0715-118">2 </span><span class="sxs-lookup"><span data-stu-id="b0715-118">2</span></span></p></td>
<td><p><span data-ttu-id="b0715-119">O registro foi inserido com o método <strong>AddNew</strong>, mas ainda não foi inserido no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0715-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0715-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="b0715-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="b0715-121">0</span><span class="sxs-lookup"><span data-stu-id="b0715-121">0</span></span></p></td>
<td><p><span data-ttu-id="b0715-122">(Padrão) O registro não foi modificado ou foi atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b0715-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

