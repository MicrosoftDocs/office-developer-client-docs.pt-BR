---
title: PositionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c2ef44c804a413b85bcf393e1487ff4423c40f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462472"
---
# <a name="positionenum"></a><span data-ttu-id="aa476-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="aa476-102">PositionEnum</span></span>


<span data-ttu-id="aa476-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa476-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa476-104">Especifica a posição atual do ponteiro do registro em um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="aa476-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa476-105">Constant</span><span class="sxs-lookup"><span data-stu-id="aa476-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aa476-106">Valor</span><span class="sxs-lookup"><span data-stu-id="aa476-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aa476-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa476-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa476-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="aa476-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="aa476-109">-2</span><span class="sxs-lookup"><span data-stu-id="aa476-109">-2</span></span></p></td>
<td><p><span data-ttu-id="aa476-110">Indica que o ponteiro de registro atual está em BOF (ou seja, a propriedade <a href="bof-eof-properties-ado.md">BOF</a> é <strong>Verdadeira</strong>).</span><span class="sxs-lookup"><span data-stu-id="aa476-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa476-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="aa476-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="aa476-112">-3</span><span class="sxs-lookup"><span data-stu-id="aa476-112">-3</span></span></p></td>
<td><p><span data-ttu-id="aa476-113">Indica que o ponteiro de registro atual está em EOF (ou seja, a propriedade <a href="bof-eof-properties-ado.md">EOF</a> é <strong>Verdadeira</strong>).</span><span class="sxs-lookup"><span data-stu-id="aa476-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa476-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="aa476-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="aa476-115">-1</span><span class="sxs-lookup"><span data-stu-id="aa476-115">-1</span></span></p></td>
<td><p><span data-ttu-id="aa476-116">Indica que o <strong>Recordset</strong> está vazio, a posição atual é desconhecida ou o provedor não oferece suporte à propriedade <a href="absolutepage-property-ado.md">AbsolutePage</a> ou <a href="absoluteposition-property-ado.md">AbsolutePosition</a>.</span><span class="sxs-lookup"><span data-stu-id="aa476-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa476-117">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="aa476-117">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="aa476-118">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="aa476-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa476-119">Constante</span><span class="sxs-lookup"><span data-stu-id="aa476-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa476-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="aa476-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa476-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="aa476-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa476-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="aa476-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

