---
title: Propriedade Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 253be078fa6a8f5fdd4cb0c6c67fc6d5385e554c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936536"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="91aba-102">Propriedade Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="91aba-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="91aba-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="91aba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91aba-p101">Retorna um valor que indique o nome da tabela que é a origem dos dados para um objeto **Field2**. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="91aba-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="91aba-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91aba-106">Syntax</span></span>

<span data-ttu-id="91aba-107">*expressão* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="91aba-107">*expression* .SourceTable</span></span>

<span data-ttu-id="91aba-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="91aba-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91aba-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="91aba-109">Remarks</span></span>

<span data-ttu-id="91aba-110">Para um objeto **Field2**, a utilização das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleta **Fields** à qual o objeto **Field2** foi acrescentado, como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="91aba-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91aba-111">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="91aba-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="91aba-112">Uso</span><span class="sxs-lookup"><span data-stu-id="91aba-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aba-113"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="91aba-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="91aba-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="91aba-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91aba-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="91aba-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="91aba-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91aba-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91aba-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="91aba-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="91aba-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91aba-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91aba-119"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="91aba-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="91aba-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="91aba-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91aba-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="91aba-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="91aba-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91aba-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91aba-p102">Estas propriedades indicam os nomes originais de campos e tabelas associados ao objeto **Field2**. Por exemplo, você pode utilizar essas propriedades para determinar a fonte original dos dados em um campo de consulta cujo nome não está relacionado ao nome do campo na tabela de base.</span><span class="sxs-lookup"><span data-stu-id="91aba-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="91aba-125">[!OBSERVAçãO] A propriedade **SourceTable** não retornará um nome de tabela significativo se utilizada em um objeto **Field2** na coleção **Fields** de um objeto **Recordset** de tipo tabela.</span><span class="sxs-lookup"><span data-stu-id="91aba-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


