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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709317"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="9c405-102">Método TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="9c405-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="9c405-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c405-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c405-104">Exclui o objeto **TableDef** especificado da coleção **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="9c405-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c405-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c405-105">Syntax</span></span>

<span data-ttu-id="9c405-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="9c405-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="9c405-107">*expressão* Uma variável que representa um objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="9c405-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c405-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c405-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c405-109">Nome</span><span class="sxs-lookup"><span data-stu-id="9c405-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9c405-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="9c405-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9c405-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9c405-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9c405-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c405-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c405-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9c405-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9c405-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9c405-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9c405-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9c405-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9c405-116">O nome de TableDef a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9c405-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9c405-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c405-117">Remarks</span></span>

<span data-ttu-id="9c405-118">O método Delete é aceito somente quando o objeto **TableDef** é novo e não tiver sido acrescentado ao banco de dados, ou quando a propriedade **Updatable** de **TableDef** está definida como **True**.</span><span class="sxs-lookup"><span data-stu-id="9c405-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

