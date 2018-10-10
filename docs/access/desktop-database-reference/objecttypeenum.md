---
title: ObjectTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38992451063e71609ab822bb231362f7a0f2cb3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462491"
---
# <a name="objecttypeenum"></a><span data-ttu-id="98641-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="98641-102">ObjectTypeEnum</span></span>


<span data-ttu-id="98641-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98641-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98641-104">Especifica o tipo de objeto de banco de dados para o qual devem ser definidas permissões ou cuja propriedade deve ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="98641-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98641-105">Constante</span><span class="sxs-lookup"><span data-stu-id="98641-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="98641-106">Valor</span><span class="sxs-lookup"><span data-stu-id="98641-106">Value</span></span></p></th>
<th><p><span data-ttu-id="98641-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="98641-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98641-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="98641-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-109">2</span><span class="sxs-lookup"><span data-stu-id="98641-109">2</span></span></p></td>
<td><p><span data-ttu-id="98641-110">O objeto é uma coluna.</span><span class="sxs-lookup"><span data-stu-id="98641-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98641-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="98641-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-112">3</span><span class="sxs-lookup"><span data-stu-id="98641-112">3</span></span></p></td>
<td><p><span data-ttu-id="98641-113">O objeto é um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="98641-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98641-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="98641-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-115">4</span><span class="sxs-lookup"><span data-stu-id="98641-115">4</span></span></p></td>
<td><p><span data-ttu-id="98641-116">O objeto é um procedimento.</span><span class="sxs-lookup"><span data-stu-id="98641-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98641-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="98641-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-118">-1</span><span class="sxs-lookup"><span data-stu-id="98641-118">-1</span></span></p></td>
<td><p><span data-ttu-id="98641-p101">O objeto é de um tipo definido pelo provedor. Ocorrerá um erro se o parâmetro <em>ObjectType</em> for <strong>adPermObjProviderSpecific</strong> e um <em>ObjectTypeId</em> não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="98641-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98641-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="98641-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-122">1</span><span class="sxs-lookup"><span data-stu-id="98641-122">1</span></span></p></td>
<td><p><span data-ttu-id="98641-123">O objeto é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="98641-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98641-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="98641-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="98641-125">5</span><span class="sxs-lookup"><span data-stu-id="98641-125">5</span></span></p></td>
<td><p><span data-ttu-id="98641-126">O objeto é um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="98641-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

