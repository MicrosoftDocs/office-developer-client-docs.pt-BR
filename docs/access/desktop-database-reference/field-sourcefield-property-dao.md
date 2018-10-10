---
title: Propriedade Field.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 729a858ae39c6403d8ccefcacaa7bade754f0484
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463379"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="95ba5-102">Propriedade Field.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="95ba5-102">Field.SourceField Property (DAO)</span></span>


<span data-ttu-id="95ba5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="95ba5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="95ba5-p101">Retorna um valor que indica o nome do campo que é a fonte de dados original de um objeto **Field**. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="95ba5-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ba5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95ba5-106">Syntax</span></span>

<span data-ttu-id="95ba5-107">*expressão* . SourceField</span><span class="sxs-lookup"><span data-stu-id="95ba5-107">*expression* .SourceField</span></span>

<span data-ttu-id="95ba5-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="95ba5-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ba5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="95ba5-109">Remarks</span></span>

<span data-ttu-id="95ba5-110">Para um objeto **Field**, o uso das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleção **Fields** à qual o objeto **Field** foi acrescentado, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="95ba5-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95ba5-111">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="95ba5-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="95ba5-112">Uso</span><span class="sxs-lookup"><span data-stu-id="95ba5-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95ba5-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="95ba5-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="95ba5-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="95ba5-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba5-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="95ba5-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="95ba5-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95ba5-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba5-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="95ba5-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="95ba5-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95ba5-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba5-119"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="95ba5-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="95ba5-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="95ba5-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba5-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="95ba5-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="95ba5-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95ba5-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95ba5-p102">Essas propriedades indicam o campo original e os nomes das tabelas associados ao objeto **Field**. Por exemplo, você pode usar essas propriedades para determinar a fonte de dados original de um campo de consulta cujo nome não está relacionado ao nome do campo na tabela base.</span><span class="sxs-lookup"><span data-stu-id="95ba5-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

