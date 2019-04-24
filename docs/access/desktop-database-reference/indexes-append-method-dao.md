---
title: Método indexes. Append (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291648"
---
# <a name="indexesappend-method-dao"></a><span data-ttu-id="5ef87-102">Método indexes. Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="5ef87-102">Indexes.Append method (DAO)</span></span>

<span data-ttu-id="5ef87-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ef87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ef87-104">Adiciona um novo **Index** à coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="5ef87-104">Adds a new **Index** to the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ef87-105">Syntax</span></span>

<span data-ttu-id="5ef87-106">*expressão* . Append (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="5ef87-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="5ef87-107">*expressão* Uma variável que representa um \*\*\*\* objeto indexes.</span><span class="sxs-lookup"><span data-stu-id="5ef87-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ef87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ef87-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ef87-109">Nome</span><span class="sxs-lookup"><span data-stu-id="5ef87-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5ef87-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="5ef87-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5ef87-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5ef87-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5ef87-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ef87-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ef87-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="5ef87-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="5ef87-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5ef87-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5ef87-115"><strong>Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="5ef87-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="5ef87-116">Uma variável objeto que representa o item que está sendo acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="5ef87-116">An object variable that represents the item being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5ef87-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ef87-117">Remarks</span></span>

<span data-ttu-id="5ef87-118">O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="5ef87-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="5ef87-119">A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5ef87-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="5ef87-120">Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="5ef87-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="5ef87-121">Por exemplo, se você não tiver especificado um tipo de campo e tentar acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , o uso do método **Append** disparará um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5ef87-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

