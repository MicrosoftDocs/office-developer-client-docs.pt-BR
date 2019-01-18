---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716427"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="ae7e0-102">Método Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae7e0-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="ae7e0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae7e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae7e0-104">Exclui o objeto **Relation** especificado da coleção **Relations**.</span><span class="sxs-lookup"><span data-stu-id="ae7e0-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae7e0-105">Syntax</span></span>

<span data-ttu-id="ae7e0-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="ae7e0-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ae7e0-107">*expressão* Uma variável que representa um objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="ae7e0-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae7e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae7e0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae7e0-109">Nome</span><span class="sxs-lookup"><span data-stu-id="ae7e0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ae7e0-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="ae7e0-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ae7e0-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ae7e0-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ae7e0-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae7e0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae7e0-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ae7e0-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ae7e0-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae7e0-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ae7e0-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ae7e0-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ae7e0-116">O nome da relação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="ae7e0-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ae7e0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae7e0-117">Remarks</span></span>

<span data-ttu-id="ae7e0-118">O método **Delete** é aceito somente quando o objeto **Relation** é um objeto novo e não acrescentado.</span><span class="sxs-lookup"><span data-stu-id="ae7e0-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

