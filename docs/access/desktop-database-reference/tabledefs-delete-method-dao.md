---
title: Método TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313990"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="d14c5-102">Método TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="d14c5-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="d14c5-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d14c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d14c5-104">Exclui o objeto **TableDef** especificado da coleção **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="d14c5-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d14c5-105">Syntax</span></span>

<span data-ttu-id="d14c5-106">*expressão* . Delete(***Name***)</span><span class="sxs-lookup"><span data-stu-id="d14c5-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="d14c5-107">*expressão* Uma variável que representa **um objeto TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="d14c5-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d14c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d14c5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d14c5-109">Nome</span><span class="sxs-lookup"><span data-stu-id="d14c5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d14c5-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="d14c5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d14c5-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d14c5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d14c5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d14c5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d14c5-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d14c5-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d14c5-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d14c5-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d14c5-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d14c5-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d14c5-116">O nome de TableDef a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d14c5-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d14c5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d14c5-117">Remarks</span></span>

<span data-ttu-id="d14c5-118">O método Delete é aceito somente quando o objeto **TableDef** é novo e não foi acrescentado ao banco de dados, ou quando a propriedade **Updatable** de **TableDef** está definida como **True**.</span><span class="sxs-lookup"><span data-stu-id="d14c5-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

