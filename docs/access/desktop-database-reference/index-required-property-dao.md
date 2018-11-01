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
ms.openlocfilehash: 71ea383cbf1c55fb15b484fea039c71c44a4e470
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881409"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="64a82-102">Propriedade Index.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="64a82-102">Index.Required Property (DAO)</span></span>


<span data-ttu-id="64a82-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="64a82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64a82-104">Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="64a82-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64a82-105">Syntax</span></span>

<span data-ttu-id="64a82-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="64a82-106">*expression* .Required</span></span>

<span data-ttu-id="64a82-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="64a82-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64a82-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="64a82-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="64a82-p101">[!OBSERVAçãO] Quando definir essa propriedade para um objeto <STRONG>Index</STRONG> ou um objeto <STRONG>Field</STRONG>, defina-a para o objeto <STRONG>Field</STRONG>. A validade da definição da propriedade para um objeto <STRONG>Field</STRONG> é verificada antes da validade do objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="64a82-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="64a82-111">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="64a82-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64a82-112">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="64a82-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="64a82-113">Então Required será</span><span class="sxs-lookup"><span data-stu-id="64a82-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64a82-114">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="64a82-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="64a82-115">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="64a82-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a82-116">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="64a82-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="64a82-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64a82-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a82-118">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="64a82-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="64a82-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64a82-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a82-120">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="64a82-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="64a82-121">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="64a82-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a82-122">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="64a82-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="64a82-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="64a82-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

