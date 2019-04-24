---
title: Propriedade RecordCount (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300767"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="16dbe-102">Propriedade RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="16dbe-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="16dbe-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16dbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16dbe-104">Indica o número de registros em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="16dbe-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="16dbe-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="16dbe-105">Return value</span></span>

<span data-ttu-id="16dbe-106">Retorna um valor **Long** que indica o número de registros no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="16dbe-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16dbe-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="16dbe-107">Remarks</span></span>

<span data-ttu-id="16dbe-p101">Utilize a propriedade **RecordCount** para saber a quantidade de registros existentes em um objeto **Recordset**. A propriedade retorna -1 quando o ADO não puder determinar o número de registros ou se um tipo de provedor ou cursornão oferecer suporte à **RecordCount**. A leitura da propriedade **RecordCount** em um **Recordset** fechado gera um erro.</span><span class="sxs-lookup"><span data-stu-id="16dbe-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="16dbe-p102">Se o objeto **Recordset** oferecer suporte a posicionamento ou indicadores aproximados  isto é, **Supports (adApproxPosition)** ou **Supports (adBookmark)**, respectivamente, ele retornará **True**  este valor será o número exato de registros do **Recordset**, independentemente de ter sido preenchido completamente. Se o objeto **Recordset** não oferecer suporte ao posicionamento aproximado, essa propriedade poderá consumir recursos de forma significativa, pois todos os registros terão que ser recuperados e contados para que um valor preciso de **RecordCount** seja retornado.</span><span class="sxs-lookup"><span data-stu-id="16dbe-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="16dbe-p103">O tipo de cursor do objeto **Recordset** será afetado se o número de registros puder ser determinado. A propriedade **RecordCount** retornará -1 para um cursor somente de encaminhamento; a contagem real de um cursor estático ou de conjunto de chaves; e -1 ou a contagem real para um cursor dinâmico, dependendo da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="16dbe-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

