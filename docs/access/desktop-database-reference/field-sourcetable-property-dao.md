---
title: Propriedade Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b29437a459d29e5238e8bd915901339d87005612
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465205"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="3ae37-102">Propriedade Field.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ae37-102">Field.SourceTable Property (DAO)</span></span>


<span data-ttu-id="3ae37-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ae37-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ae37-p101">Retorna um valor que indica o nome da tabela que é a fonte de dados original de um objeto **Field**. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3ae37-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae37-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ae37-106">Syntax</span></span>

<span data-ttu-id="3ae37-107">*expressão* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="3ae37-107">*expression* .SourceTable</span></span>

<span data-ttu-id="3ae37-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="3ae37-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae37-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ae37-109">Remarks</span></span>

<span data-ttu-id="3ae37-110">Para um objeto **Field**, o uso das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleção **Fields** à qual o objeto **Field** foi acrescentado, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ae37-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ae37-111">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="3ae37-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="3ae37-112">Uso</span><span class="sxs-lookup"><span data-stu-id="3ae37-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ae37-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3ae37-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="3ae37-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3ae37-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ae37-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3ae37-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3ae37-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ae37-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ae37-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3ae37-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="3ae37-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ae37-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ae37-119"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="3ae37-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="3ae37-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3ae37-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ae37-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3ae37-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3ae37-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ae37-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ae37-p102">Essas propriedades indicam o campo original e os nomes das tabelas associados ao objeto **Field**. Por exemplo, você pode usar essas propriedades para determinar a fonte de dados original de um campo de consulta cujo nome não está relacionado ao nome do campo na tabela base.</span><span class="sxs-lookup"><span data-stu-id="3ae37-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3ae37-125">[!OBSERVAçãO] A propriedade <STRONG>SourceTable</STRONG> não retornará um nome de tabela significativo se for usado em um objeto <STRONG>Field</STRONG> na coleção <STRONG>Fields</STRONG> de um objeto <STRONG>Recordset</STRONG> do tipo tabela.</span><span class="sxs-lookup"><span data-stu-id="3ae37-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


