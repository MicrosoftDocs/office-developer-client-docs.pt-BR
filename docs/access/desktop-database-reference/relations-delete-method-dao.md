---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462581e5b1ab3f09b697ee7f4b763a889d8119fd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925524"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="ed55d-102">Método Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed55d-102">Relations.Delete method (DAO)</span></span>


<span data-ttu-id="ed55d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed55d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed55d-104">Exclui o objeto **Relation** especificado da coleção **Relations**.</span><span class="sxs-lookup"><span data-stu-id="ed55d-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed55d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed55d-105">Syntax</span></span>

<span data-ttu-id="ed55d-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="ed55d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ed55d-107">*expressão* Uma variável que representa um objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="ed55d-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ed55d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed55d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed55d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="ed55d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ed55d-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="ed55d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ed55d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ed55d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ed55d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed55d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed55d-113">Name</span><span class="sxs-lookup"><span data-stu-id="ed55d-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ed55d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ed55d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ed55d-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="ed55d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ed55d-116">O nome da relação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="ed55d-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ed55d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed55d-117">Remarks</span></span>

<span data-ttu-id="ed55d-118">O método **Delete** é aceito somente quando o objeto **Relation** é um objeto novo e não acrescentado.</span><span class="sxs-lookup"><span data-stu-id="ed55d-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

