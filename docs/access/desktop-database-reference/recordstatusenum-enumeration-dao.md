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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710500"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="8dde7-102">Enumeração RecordStatusEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="8dde7-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="8dde7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dde7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8dde7-104">Usada com a propriedade **RecordStatus** para indicar o status de atualização do registro atual, se ele fizer parte de uma atualização em lotes.</span><span class="sxs-lookup"><span data-stu-id="8dde7-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8dde7-105">Nome</span><span class="sxs-lookup"><span data-stu-id="8dde7-105">Name</span></span></p></th>
<th><p><span data-ttu-id="8dde7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8dde7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8dde7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dde7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dde7-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="8dde7-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="8dde7-109">4</span><span class="sxs-lookup"><span data-stu-id="8dde7-109">4</span></span></p></td>
<td><p><span data-ttu-id="8dde7-110">O registro foi excluído localmente e no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8dde7-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dde7-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="8dde7-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="8dde7-112">3</span><span class="sxs-lookup"><span data-stu-id="8dde7-112">3</span></span></p></td>
<td><p><span data-ttu-id="8dde7-113">O registro foi excluído, mas ainda não foi excluído do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8dde7-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dde7-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="8dde7-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="8dde7-115">1</span><span class="sxs-lookup"><span data-stu-id="8dde7-115">1</span></span></p></td>
<td><p><span data-ttu-id="8dde7-116">O registro foi modificado e não foi atualizado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8dde7-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dde7-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="8dde7-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="8dde7-118">2</span><span class="sxs-lookup"><span data-stu-id="8dde7-118">2</span></span></p></td>
<td><p><span data-ttu-id="8dde7-119">O registro foi inserido com o método <strong>AddNew</strong>, mas ainda não foi inserido no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8dde7-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dde7-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="8dde7-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="8dde7-121">0</span><span class="sxs-lookup"><span data-stu-id="8dde7-121">0</span></span></p></td>
<td><p><span data-ttu-id="8dde7-122">(Padrão) O registro não foi modificado ou foi atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8dde7-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

