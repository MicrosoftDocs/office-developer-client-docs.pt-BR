---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282849"
---
# <a name="adcprop_updatecriteria_enum"></a><span data-ttu-id="54320-102">ADCPROP \_ UPDATECRITERIA \_ ENUM</span><span class="sxs-lookup"><span data-stu-id="54320-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="54320-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54320-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54320-104">Especifica quais campos podem ser usados para detectar conflitos durante uma atualização otimista de uma linha da fonte de dados com um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="54320-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="54320-105">Use essas constantes com a propriedade dinâmica  "**Update Criteria**"  do **Recordset**, mencionada no [Índice de Propriedade Dinâmica ADO](ado-dynamic-property-index.md) e documentada no [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="54320-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54320-106">Constant</span><span class="sxs-lookup"><span data-stu-id="54320-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="54320-107">Valor</span><span class="sxs-lookup"><span data-stu-id="54320-107">Value</span></span></p></th>
<th><p><span data-ttu-id="54320-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="54320-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54320-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="54320-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="54320-110">1 </span><span class="sxs-lookup"><span data-stu-id="54320-110">1</span></span></p></td>
<td><p><span data-ttu-id="54320-111">Detecta conflitos se qualquer coluna da linha da fonte de dados tiver sido alterada.</span><span class="sxs-lookup"><span data-stu-id="54320-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54320-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="54320-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="54320-113">0</span><span class="sxs-lookup"><span data-stu-id="54320-113">0</span></span></p></td>
<td><p><span data-ttu-id="54320-114">Detecta conflitos se a coluna de chaves da linha da fonte de dados tiver sido alterada, o que significa que a linha foi excluída.</span><span class="sxs-lookup"><span data-stu-id="54320-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54320-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="54320-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="54320-116">3 </span><span class="sxs-lookup"><span data-stu-id="54320-116">3</span></span></p></td>
<td><p><span data-ttu-id="54320-117">Detecta conflitos se o carimbo de data/hora da linha da fonte de dados tiver sido alterada, o que significa que a linha foi acessada depois que o <strong>Recordset</strong> foi obtido.</span><span class="sxs-lookup"><span data-stu-id="54320-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54320-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="54320-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="54320-119">2 </span><span class="sxs-lookup"><span data-stu-id="54320-119">2</span></span></p></td>
<td><p><span data-ttu-id="54320-120">Detecta conflitos se alguma das colunas da linha da fonte de dados que corresponde aos campos atualizados do <strong>Recordset</strong> tiverem sido alteradas.</span><span class="sxs-lookup"><span data-stu-id="54320-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="54320-121">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="54320-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="54320-122">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="54320-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54320-123">Constant</span><span class="sxs-lookup"><span data-stu-id="54320-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54320-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="54320-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54320-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="54320-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54320-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="54320-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54320-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="54320-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

