---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b9c1aff21b62eff061a3f68ef3ad56e07e46388d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860081"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="29b31-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="29b31-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="29b31-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="29b31-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="29b31-104">Especifica quando o provedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcula colunas calculadas e agregadas em um Recordset hierárquico.</span><span class="sxs-lookup"><span data-stu-id="29b31-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="29b31-105">Essas constantes são usadas somente com o provedor **MSDataShape** e a **Recordset** "**Auto Recalc**" propriedade dinâmica, que é referenciada no [Índice de propriedades dinâmicas ADO](ado-dynamic-property-index.md) e documentada no [Microsoft Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou a documentação do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="29b31-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29b31-106">Constant</span><span class="sxs-lookup"><span data-stu-id="29b31-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="29b31-107">Valor</span><span class="sxs-lookup"><span data-stu-id="29b31-107">Value</span></span></p></th>
<th><p><span data-ttu-id="29b31-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="29b31-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29b31-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="29b31-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="29b31-110">1</span><span class="sxs-lookup"><span data-stu-id="29b31-110">1</span></span></p></td>
<td><p><span data-ttu-id="29b31-p101">Padrão. Recalcula sempre que determinados valores do provedor <strong>MSDataShape</strong>, dos quais as colunas calculadas dependem, são alterados.</span><span class="sxs-lookup"><span data-stu-id="29b31-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b31-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="29b31-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="29b31-114">0</span><span class="sxs-lookup"><span data-stu-id="29b31-114">0</span></span></p></td>
<td><p><span data-ttu-id="29b31-115">Calcula apenas quando cria-se inicialmente o <strong>Recordset</strong> hierárquico.</span><span class="sxs-lookup"><span data-stu-id="29b31-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="29b31-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="29b31-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="29b31-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="29b31-117">These constants do not have ADO/WFC equivalents.</span></span>

