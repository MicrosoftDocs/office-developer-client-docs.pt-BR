---
title: Método QueryDefs.Append (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7fcd5cb9e018836a53d90d77281cf762bc625dda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462408"
---
# <a name="querydefsappend-method-dao"></a><span data-ttu-id="641a2-102">Método QueryDefs.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="641a2-102">QueryDefs.Append Method (DAO)</span></span>


<span data-ttu-id="641a2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="641a2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="641a2-104">Adiciona um novo **QueryDef** à coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="641a2-104">Adds a new **QueryDef** to the **QueryDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="641a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="641a2-105">Syntax</span></span>

<span data-ttu-id="641a2-106">*expressão* . Acrescentar (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="641a2-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="641a2-107">*expressão* Uma variável que representa um objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="641a2-107">*expression* A variable that represents a **QueryDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="641a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="641a2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="641a2-109">Nome</span><span class="sxs-lookup"><span data-stu-id="641a2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="641a2-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="641a2-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="641a2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="641a2-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="641a2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="641a2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="641a2-113">Objeto</span><span class="sxs-lookup"><span data-stu-id="641a2-113">Object</span></span></p></td>
<td><p><span data-ttu-id="641a2-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="641a2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="641a2-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="641a2-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="641a2-116">Uma variável de objeto que representa o campo sendo acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="641a2-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="641a2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="641a2-117">Remarks</span></span>

<span data-ttu-id="641a2-118">O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="641a2-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="641a2-119">A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="641a2-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="641a2-120">Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro.</span><span class="sxs-lookup"><span data-stu-id="641a2-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="641a2-121">Por exemplo, se você ainda não tiver especificado um tipo de campo e, então, tenta acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , usar o método **Append** dispara um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="641a2-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

