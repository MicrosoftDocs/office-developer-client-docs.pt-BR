---
title: Propriedade Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb0c7b57b8ad5c0a1c202197e14fdaefd9a1103f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881017"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="4deb6-102">Propriedade Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="4deb6-102">Field2.SourceTable Property (DAO)</span></span>


<span data-ttu-id="4deb6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4deb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4deb6-p101">Retorna um valor que indique o nome da tabela que é a origem dos dados para um objeto **Field2**. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4deb6-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4deb6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4deb6-106">Syntax</span></span>

<span data-ttu-id="4deb6-107">*expressão* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="4deb6-107">*expression* .SourceTable</span></span>

<span data-ttu-id="4deb6-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="4deb6-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4deb6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4deb6-109">Remarks</span></span>

<span data-ttu-id="4deb6-110">Para um objeto **Field2**, a utilização das propriedades **SourceField** e **SourceTable** depende do objeto que contém a coleta **Fields** à qual o objeto **Field2** foi acrescentado, como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4deb6-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4deb6-111">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="4deb6-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4deb6-112">Uso</span><span class="sxs-lookup"><span data-stu-id="4deb6-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb6-113"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="4deb6-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb6-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4deb6-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb6-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4deb6-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb6-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4deb6-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb6-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4deb6-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb6-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4deb6-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb6-119"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="4deb6-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb6-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4deb6-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb6-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4deb6-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb6-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4deb6-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb6-p102">Estas propriedades indicam os nomes originais de campos e tabelas associados ao objeto **Field2**. Por exemplo, você pode utilizar essas propriedades para determinar a fonte original dos dados em um campo de consulta cujo nome não está relacionado ao nome do campo na tabela de base.</span><span class="sxs-lookup"><span data-stu-id="4deb6-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4deb6-125">[!OBSERVAçãO] A propriedade <STRONG>SourceTable</STRONG> não retornará um nome de tabela significativo se utilizada em um objeto <STRONG>Field2</STRONG> na coleção <STRONG>Fields</STRONG> de um objeto <STRONG>Recordset</STRONG> de tipo tabela.</span><span class="sxs-lookup"><span data-stu-id="4deb6-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


