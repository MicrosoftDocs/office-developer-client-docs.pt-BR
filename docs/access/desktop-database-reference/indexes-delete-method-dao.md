---
title: Método Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66f08fa9733de0b63ca8bb659972abbc59183e16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922318"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="39957-102">Método Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="39957-102">Indexes.Delete method (DAO)</span></span>


<span data-ttu-id="39957-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="39957-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39957-104">Exclui o **Index** especificado da coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="39957-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="39957-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39957-105">Syntax</span></span>

<span data-ttu-id="39957-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="39957-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="39957-107">*expressão* Uma variável que representa um objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="39957-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="39957-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39957-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39957-109">Nome</span><span class="sxs-lookup"><span data-stu-id="39957-109">Name</span></span></p></th>
<th><p><span data-ttu-id="39957-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="39957-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="39957-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="39957-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="39957-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="39957-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39957-113">Name</span><span class="sxs-lookup"><span data-stu-id="39957-113">Name</span></span></p></td>
<td><p><span data-ttu-id="39957-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="39957-114">Required</span></span></p></td>
<td><p><span data-ttu-id="39957-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="39957-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="39957-116">O nome do índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="39957-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="39957-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="39957-117">Remarks</span></span>

<span data-ttu-id="39957-118">O método **Delete** é suportado somente quando o objeto **Index** for novo e não tiver sido acrescentado ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39957-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

