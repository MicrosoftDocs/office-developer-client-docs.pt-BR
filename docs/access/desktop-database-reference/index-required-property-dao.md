---
title: Propriedade Index.Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0797ed5f930d4475d03f492109c977f8494591ce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464482"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="2364d-102">Propriedade Index.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="2364d-102">Index.Required Property (DAO)</span></span>


<span data-ttu-id="2364d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2364d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2364d-104">Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="2364d-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2364d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2364d-105">Syntax</span></span>

<span data-ttu-id="2364d-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="2364d-106">*expression* .Required</span></span>

<span data-ttu-id="2364d-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="2364d-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2364d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2364d-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="2364d-p101">[!OBSERVAçãO] Quando definir essa propriedade para um objeto <STRONG>Index</STRONG> ou um objeto <STRONG>Field</STRONG>, defina-a para o objeto <STRONG>Field</STRONG>. A validade da definição da propriedade para um objeto <STRONG>Field</STRONG> é verificada antes da validade do objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2364d-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="2364d-111">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2364d-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2364d-112">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="2364d-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="2364d-113">Então Required será</span><span class="sxs-lookup"><span data-stu-id="2364d-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2364d-114">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="2364d-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2364d-115">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="2364d-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2364d-116">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="2364d-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2364d-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2364d-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2364d-118">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="2364d-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2364d-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2364d-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2364d-120">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="2364d-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2364d-121">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="2364d-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2364d-122">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="2364d-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="2364d-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2364d-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

