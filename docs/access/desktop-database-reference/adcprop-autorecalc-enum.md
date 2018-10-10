---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc02e8cde556a70ca6b2c72f056d218904c31ec2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465003"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="f4475-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="f4475-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="f4475-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4475-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4475-104">Especifica quando o provedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcula colunas calculadas e agregadas em um Recordset hierárquico.</span><span class="sxs-lookup"><span data-stu-id="f4475-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="f4475-105">Essas constantes são usadas somente com o provedor **MSDataShape** e a **Recordset** "**Auto Recalc**" propriedade dinâmica, que é referenciada no [Índice de propriedades dinâmicas ADO](ado-dynamic-property-index.md) e documentada no [Microsoft Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou a documentação do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="f4475-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4475-106">Constant</span><span class="sxs-lookup"><span data-stu-id="f4475-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f4475-107">Valor</span><span class="sxs-lookup"><span data-stu-id="f4475-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f4475-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4475-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4475-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="f4475-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="f4475-110">1</span><span class="sxs-lookup"><span data-stu-id="f4475-110">1</span></span></p></td>
<td><p><span data-ttu-id="f4475-p101">Padrão. Recalcula sempre que determinados valores do provedor <strong>MSDataShape</strong>, dos quais as colunas calculadas dependem, são alterados.</span><span class="sxs-lookup"><span data-stu-id="f4475-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4475-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="f4475-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="f4475-114">0</span><span class="sxs-lookup"><span data-stu-id="f4475-114">0</span></span></p></td>
<td><p><span data-ttu-id="f4475-115">Calcula apenas quando cria-se inicialmente o <strong>Recordset</strong> hierárquico.</span><span class="sxs-lookup"><span data-stu-id="f4475-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4475-116">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="f4475-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f4475-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f4475-117">These constants do not have ADO/WFC equivalents.</span></span>

