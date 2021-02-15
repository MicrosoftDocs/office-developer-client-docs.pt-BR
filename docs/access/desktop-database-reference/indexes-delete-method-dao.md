---
title: Método Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291549"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="2cf07-102">Método Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="2cf07-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="2cf07-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cf07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2cf07-104">Exclui o **Index** especificado da coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="2cf07-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cf07-105">Syntax</span></span>

<span data-ttu-id="2cf07-106">*expressão* . Delete(***Name***)</span><span class="sxs-lookup"><span data-stu-id="2cf07-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="2cf07-107">*expressão* Uma variável que representa um **objeto Indexes** .</span><span class="sxs-lookup"><span data-stu-id="2cf07-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cf07-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cf07-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cf07-109">Nome</span><span class="sxs-lookup"><span data-stu-id="2cf07-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2cf07-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="2cf07-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2cf07-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2cf07-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2cf07-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cf07-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cf07-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2cf07-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2cf07-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2cf07-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2cf07-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2cf07-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf07-116">O nome do índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2cf07-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2cf07-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cf07-117">Remarks</span></span>

<span data-ttu-id="2cf07-118">O método **Delete** tem suporte apenas quando o objeto **Index** for novo e não tiver sido acrescentado ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2cf07-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

