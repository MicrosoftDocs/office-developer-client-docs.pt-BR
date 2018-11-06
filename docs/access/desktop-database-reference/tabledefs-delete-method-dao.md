---
title: Método TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999005"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="70e25-102">Método TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="70e25-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="70e25-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="70e25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70e25-104">Exclui o objeto **TableDef** especificado da coleção **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="70e25-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e25-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70e25-105">Syntax</span></span>

<span data-ttu-id="70e25-106">*expressão* . Excluir (***nome***)</span><span class="sxs-lookup"><span data-stu-id="70e25-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="70e25-107">*expressão* Uma variável que representa um objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="70e25-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="70e25-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70e25-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70e25-109">Nome</span><span class="sxs-lookup"><span data-stu-id="70e25-109">Name</span></span></p></th>
<th><p><span data-ttu-id="70e25-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="70e25-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="70e25-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="70e25-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="70e25-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="70e25-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70e25-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="70e25-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="70e25-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="70e25-114">Required</span></span></p></td>
<td><p><span data-ttu-id="70e25-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="70e25-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70e25-116">O nome de TableDef a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="70e25-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="70e25-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="70e25-117">Remarks</span></span>

<span data-ttu-id="70e25-118">O método Delete é aceito somente quando o objeto **TableDef** é novo e não tiver sido acrescentado ao banco de dados, ou quando a propriedade **Updatable** de **TableDef** está definida como **True**.</span><span class="sxs-lookup"><span data-stu-id="70e25-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

