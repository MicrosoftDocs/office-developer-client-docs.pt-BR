---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280519"
---
# <a name="adcprop_autorecalc_enum"></a><span data-ttu-id="ba3b3-102">ADCPROP \_ AUTORECALC \_ ENUM</span><span class="sxs-lookup"><span data-stu-id="ba3b3-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="ba3b3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba3b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba3b3-104">Especifica quando o provedor [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcula colunas calculadas e agregadas em um Recordset hierárquico.</span><span class="sxs-lookup"><span data-stu-id="ba3b3-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="ba3b3-105">Essas constantes são usadas apenas com o provedor **MSDataShape** e a propriedade dinâmica "**Auto Recalc**" do **Recordset,** que é referenciada no Índice de Propriedades Dinâmicas do [ADO](ado-dynamic-property-index.md) e documentada no [Microsoft Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou Microsoft Data Shaping Service para documentação do [OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ba3b3-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba3b3-106">Constant</span><span class="sxs-lookup"><span data-stu-id="ba3b3-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="ba3b3-107">Valor</span><span class="sxs-lookup"><span data-stu-id="ba3b3-107">Value</span></span></p></th>
<th><p><span data-ttu-id="ba3b3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba3b3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba3b3-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="ba3b3-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="ba3b3-110">1 </span><span class="sxs-lookup"><span data-stu-id="ba3b3-110">1</span></span></p></td>
<td><p><span data-ttu-id="ba3b3-p101">Padrão. Recalcula sempre que determinados valores do provedor <strong>MSDataShape</strong>, dos quais as colunas calculadas dependem, são alterados.</span><span class="sxs-lookup"><span data-stu-id="ba3b3-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba3b3-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="ba3b3-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="ba3b3-114">0</span><span class="sxs-lookup"><span data-stu-id="ba3b3-114">0</span></span></p></td>
<td><p><span data-ttu-id="ba3b3-115">Calcula apenas quando cria-se inicialmente o <strong>Recordset</strong> hierárquico.</span><span class="sxs-lookup"><span data-stu-id="ba3b3-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ba3b3-116">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ba3b3-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="ba3b3-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="ba3b3-117">These constants do not have ADO/WFC equivalents.</span></span>

