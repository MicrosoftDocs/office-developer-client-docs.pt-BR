---
title: Propriedades dinâmicas do conjunto de registros em XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946955"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="42b23-102">Propriedades dinâmicas do conjunto de registros em XML</span><span class="sxs-lookup"><span data-stu-id="42b23-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="42b23-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="42b23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42b23-104">As propriedades específicas do provedor do **Recordset** a seguir (do Mecanismo de cursor do cliente) são mantidas atualmente no formato XML:</span><span class="sxs-lookup"><span data-stu-id="42b23-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="42b23-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="42b23-105">**AutoRecalc**</span></span>
- <span data-ttu-id="42b23-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="42b23-106">**BatchSize**</span></span>
- <span data-ttu-id="42b23-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="42b23-107">**CommandTimeout**</span></span>
- <span data-ttu-id="42b23-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="42b23-108">**IRowsetChange**</span></span>
- <span data-ttu-id="42b23-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="42b23-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="42b23-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="42b23-110">**Reshape Name**</span></span>
- <span data-ttu-id="42b23-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="42b23-111">**Resync Command**</span></span>
- <span data-ttu-id="42b23-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="42b23-112">**Unique Catalog**</span></span>
- <span data-ttu-id="42b23-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="42b23-113">**Unique Schema**</span></span>
- <span data-ttu-id="42b23-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="42b23-114">**Unique Table**</span></span>
- <span data-ttu-id="42b23-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="42b23-115">**Update Resync**</span></span>
- <span data-ttu-id="42b23-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="42b23-116">**UpdateCriteria**</span></span>


<span data-ttu-id="42b23-p101">Essas propriedades são salvas na seção de esquema como atributos da definição do elemento do **Recordset** que está sendo mantido. Esses atributos são definidos no namespace do esquema do conjunto de linhas e deve ter o prefixo "rs:".</span><span class="sxs-lookup"><span data-stu-id="42b23-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="42b23-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="42b23-119">See also</span></span>

- [<span data-ttu-id="42b23-120">Propriedades dinâmicas do ADO</span><span class="sxs-lookup"><span data-stu-id="42b23-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)