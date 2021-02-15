---
title: Método TableDefs.Append (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31eca3f4ca5993a401bd85a4b04299a8697c16e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314375"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="51a7d-102">Método TableDefs.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="51a7d-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="51a7d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51a7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51a7d-104">Adiciona um novo objeto **TableDef** à coleção **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="51a7d-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51a7d-105">Syntax</span></span>

<span data-ttu-id="51a7d-106">*expressão* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="51a7d-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="51a7d-107">*expressão* Uma variável que representa **um objeto TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="51a7d-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="51a7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51a7d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51a7d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="51a7d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="51a7d-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="51a7d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="51a7d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="51a7d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="51a7d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51a7d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51a7d-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="51a7d-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="51a7d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51a7d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="51a7d-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="51a7d-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="51a7d-116">Uma variável de objeto que representa o campo sendo acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="51a7d-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="51a7d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51a7d-117">Remarks</span></span>

<span data-ttu-id="51a7d-118">O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="51a7d-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="51a7d-119">A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51a7d-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="51a7d-120">Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="51a7d-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="51a7d-121">Por exemplo, se você não especificou um tipo de campo e tentou acrescentar o objeto **Field** a uma coleção **Fields** em um objeto **TableDef**, a utilização do método **Append** aciona um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="51a7d-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

