---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998921"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="b3fd3-102">Método Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3fd3-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="b3fd3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3fd3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3fd3-104">Exclui o objeto **Relation** especificado da coleção **Relations**.</span><span class="sxs-lookup"><span data-stu-id="b3fd3-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3fd3-105">Syntax</span></span>

<span data-ttu-id="b3fd3-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="b3fd3-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="b3fd3-107">*expressão* Uma variável que representa um objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="b3fd3-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3fd3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3fd3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3fd3-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fd3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b3fd3-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="b3fd3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b3fd3-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b3fd3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b3fd3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3fd3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3fd3-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="b3fd3-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b3fd3-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b3fd3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b3fd3-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="b3fd3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fd3-116">O nome da relação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="b3fd3-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b3fd3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3fd3-117">Remarks</span></span>

<span data-ttu-id="b3fd3-118">O método **Delete** é aceito somente quando o objeto **Relation** é um objeto novo e não acrescentado.</span><span class="sxs-lookup"><span data-stu-id="b3fd3-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

