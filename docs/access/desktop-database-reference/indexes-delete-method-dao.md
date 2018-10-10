---
title: Método Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462835"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="93a5d-102">Método Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="93a5d-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="93a5d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="93a5d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="93a5d-104">Exclui o **Index** especificado da coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="93a5d-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93a5d-105">Syntax</span></span>

<span data-ttu-id="93a5d-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="93a5d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="93a5d-107">*expressão* Uma variável que representa um objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="93a5d-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="93a5d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93a5d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93a5d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="93a5d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="93a5d-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="93a5d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="93a5d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="93a5d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="93a5d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="93a5d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93a5d-113">Name</span><span class="sxs-lookup"><span data-stu-id="93a5d-113">Name</span></span></p></td>
<td><p><span data-ttu-id="93a5d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="93a5d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="93a5d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="93a5d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="93a5d-116">O nome do índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="93a5d-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="93a5d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="93a5d-117">Remarks</span></span>

<span data-ttu-id="93a5d-118">O método **Delete** é suportado somente quando o objeto **Index** for novo e não tiver sido acrescentado ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="93a5d-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

