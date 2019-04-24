---
title: Propriedade index. Required (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291696"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="d7ede-102">Propriedade index. Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7ede-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="d7ede-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7ede-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7ede-104">Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="d7ede-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ede-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7ede-105">Syntax</span></span>

<span data-ttu-id="d7ede-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="d7ede-106">*expression* .Required</span></span>

<span data-ttu-id="d7ede-107">*expressão* Uma variável que representa um objeto **index** .</span><span class="sxs-lookup"><span data-stu-id="d7ede-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ede-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7ede-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="d7ede-p101">[!OBSERVAçãO] Quando definir essa propriedade para um objeto **Index** ou um objeto **Field**, defina-a para o objeto **Field**. A validade da definição da propriedade para um objeto **Field** é verificada antes da validade do objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="d7ede-p101">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="d7ede-111">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7ede-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7ede-112">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="d7ede-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="d7ede-113">Então Required será</span><span class="sxs-lookup"><span data-stu-id="d7ede-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7ede-114">
						Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d7ede-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d7ede-115">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="d7ede-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ede-116">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="d7ede-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d7ede-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7ede-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ede-118">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d7ede-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d7ede-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7ede-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ede-120">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="d7ede-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d7ede-121">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="d7ede-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ede-122">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d7ede-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="d7ede-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d7ede-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

