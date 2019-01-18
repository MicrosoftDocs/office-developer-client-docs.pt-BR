---
title: Método Workspaces.Append (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718879"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="bbe0b-102">Método Workspaces.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbe0b-102">Workspaces.Append method (DAO)</span></span>

<span data-ttu-id="bbe0b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbe0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbe0b-104">Adiciona um novo objeto **Workspace** à coleção **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe0b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbe0b-105">Syntax</span></span>

<span data-ttu-id="bbe0b-106">*expressão* . Acrescentar (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="bbe0b-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="bbe0b-107">*expressão* Uma variável que representa um objeto **Workspaces** .</span><span class="sxs-lookup"><span data-stu-id="bbe0b-107">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbe0b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbe0b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbe0b-109">Nome</span><span class="sxs-lookup"><span data-stu-id="bbe0b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bbe0b-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="bbe0b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="bbe0b-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bbe0b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="bbe0b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbe0b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe0b-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="bbe0b-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="bbe0b-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bbe0b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="bbe0b-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="bbe0b-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="bbe0b-116">Uma variável de objeto que representa o campo sendo acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bbe0b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbe0b-117">Remarks</span></span>

<span data-ttu-id="bbe0b-118">O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="bbe0b-119">A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="bbe0b-120">Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="bbe0b-121">Por exemplo, se você ainda não tiver especificado um tipo de campo e, então, tenta acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , usar o método **Append** dispara um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bbe0b-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

