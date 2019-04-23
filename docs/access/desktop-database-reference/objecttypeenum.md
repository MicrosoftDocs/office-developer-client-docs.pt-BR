---
title: ObjectTypeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288529"
---
# <a name="objecttypeenum"></a><span data-ttu-id="d052b-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="d052b-102">ObjectTypeEnum</span></span>

<span data-ttu-id="d052b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d052b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d052b-104">Especifica o tipo de objeto de banco de dados para o qual devem ser definidas permissões ou cuja propriedade deve ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="d052b-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d052b-105">Constant</span><span class="sxs-lookup"><span data-stu-id="d052b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d052b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d052b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d052b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d052b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d052b-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-109">duas</span><span class="sxs-lookup"><span data-stu-id="d052b-109">2</span></span></p></td>
<td><p><span data-ttu-id="d052b-110">O objeto é uma coluna.</span><span class="sxs-lookup"><span data-stu-id="d052b-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d052b-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-112">3D</span><span class="sxs-lookup"><span data-stu-id="d052b-112">3</span></span></p></td>
<td><p><span data-ttu-id="d052b-113">O objeto é um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d052b-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d052b-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-115">quatro</span><span class="sxs-lookup"><span data-stu-id="d052b-115">4</span></span></p></td>
<td><p><span data-ttu-id="d052b-116">O objeto é um procedimento.</span><span class="sxs-lookup"><span data-stu-id="d052b-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d052b-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-118">-1</span><span class="sxs-lookup"><span data-stu-id="d052b-118">-1</span></span></p></td>
<td><p><span data-ttu-id="d052b-p101">O objeto é de um tipo definido pelo provedor. Ocorrerá um erro se o parâmetro <em>ObjectType</em> for <strong>adPermObjProviderSpecific</strong> e um <em>ObjectTypeId</em> não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="d052b-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d052b-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-122">1</span><span class="sxs-lookup"><span data-stu-id="d052b-122">1</span></span></p></td>
<td><p><span data-ttu-id="d052b-123">O objeto é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="d052b-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d052b-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="d052b-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="d052b-125">0,5</span><span class="sxs-lookup"><span data-stu-id="d052b-125">5</span></span></p></td>
<td><p><span data-ttu-id="d052b-126">O objeto é um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="d052b-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

