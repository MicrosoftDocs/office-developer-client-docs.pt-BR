---
title: AllowNullsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c4c44771258cd94700bfb2902cf8bdad47a2d712
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860137"
---
# <a name="allownullsenum"></a><span data-ttu-id="6b368-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="6b368-102">AllowNullsEnum</span></span>

<span data-ttu-id="6b368-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b368-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6b368-104">Especifica se os registros com valores nulos são indexados.</span><span class="sxs-lookup"><span data-stu-id="6b368-104">Specifies whether records with null values are indexed.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b368-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6b368-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6b368-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6b368-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6b368-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b368-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b368-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="6b368-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="6b368-109">0</span><span class="sxs-lookup"><span data-stu-id="6b368-109">0</span></span></p></td>
<td><p><span data-ttu-id="6b368-p101">O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, a entrada será inserida no índice.</span><span class="sxs-lookup"><span data-stu-id="6b368-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b368-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="6b368-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="6b368-113">1</span><span class="sxs-lookup"><span data-stu-id="6b368-113">1</span></span></p></td>
<td><p><span data-ttu-id="6b368-p102">Padrão. O índice não permite entradas nas quais as colunas chave são nulas. Se for inserido um valor nulo em uma dessas colunas, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6b368-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b368-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="6b368-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="6b368-118">2</span><span class="sxs-lookup"><span data-stu-id="6b368-118">2</span></span></p></td>
<td><p><span data-ttu-id="6b368-p103">O índice não insere entradas que contenham chaves nulas. Se for inserido um valor nulo em uma coluna chave, a entrada será ignorada e não ocorrerá nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="6b368-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b368-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="6b368-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="6b368-122">4</span><span class="sxs-lookup"><span data-stu-id="6b368-122">4</span></span></p></td>
<td><p><span data-ttu-id="6b368-p104">O índice não insere entradas onde alguma coluna chave contenha um valor nulo. Em um índice com uma chave de várias colunas, se for inserido um valor nulo em alguma coluna, a entrada será ignorada e não ocorrerá nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="6b368-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

