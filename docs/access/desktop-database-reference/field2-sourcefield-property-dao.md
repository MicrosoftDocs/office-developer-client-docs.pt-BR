---
title: Propriedade Field2.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09351acfea263c41bd9cb7f857139dfacf359421
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463613"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="df807-102">Propriedade Field2.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="df807-102">Field2.SourceField Property (DAO)</span></span>


<span data-ttu-id="df807-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df807-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="df807-p101">Retorna um valor que indique o nome do campo que é a origem dos dados para um objeto **Field2**. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df807-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df807-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df807-106">Syntax</span></span>

<span data-ttu-id="df807-107">*expressão* . SourceField</span><span class="sxs-lookup"><span data-stu-id="df807-107">*expression* .SourceField</span></span>

<span data-ttu-id="df807-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="df807-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df807-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="df807-109">Remarks</span></span>

<span data-ttu-id="df807-110">Para um objeto **Field2**, a utilização das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleta **Fields** à qual o objeto **Field2** foi acrescentado, como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="df807-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df807-111">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="df807-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="df807-112">Uso</span><span class="sxs-lookup"><span data-stu-id="df807-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df807-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="df807-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="df807-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="df807-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df807-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="df807-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="df807-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df807-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df807-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="df807-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="df807-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df807-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df807-119"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="df807-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="df807-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="df807-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df807-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="df807-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="df807-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df807-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df807-p102">Estas propriedades indicam os nomes originais de campos e tabelas associados ao objeto **Field2**. Por exemplo, você pode utilizar essas propriedades para determinar a fonte original dos dados em um campo de consulta cujo nome não está relacionado ao nome do campo na tabela de base.</span><span class="sxs-lookup"><span data-stu-id="df807-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

