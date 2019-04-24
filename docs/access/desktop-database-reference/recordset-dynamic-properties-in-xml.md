---
title: Propriedades dinâmicas do conjunto de registros em XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307655"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="e7278-102">Propriedades dinâmicas do conjunto de registros em XML</span><span class="sxs-lookup"><span data-stu-id="e7278-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="e7278-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7278-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7278-104">As propriedades específicas do provedor do **Recordset** a seguir (do Mecanismo de cursor do cliente) são mantidas atualmente no formato XML:</span><span class="sxs-lookup"><span data-stu-id="e7278-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="e7278-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="e7278-105">**AutoRecalc**</span></span>
- <span data-ttu-id="e7278-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="e7278-106">**BatchSize**</span></span>
- <span data-ttu-id="e7278-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="e7278-107">**CommandTimeout**</span></span>
- <span data-ttu-id="e7278-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="e7278-108">**IRowsetChange**</span></span>
- <span data-ttu-id="e7278-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="e7278-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="e7278-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="e7278-110">**Reshape Name**</span></span>
- <span data-ttu-id="e7278-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="e7278-111">**Resync Command**</span></span>
- <span data-ttu-id="e7278-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="e7278-112">**Unique Catalog**</span></span>
- <span data-ttu-id="e7278-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="e7278-113">**Unique Schema**</span></span>
- <span data-ttu-id="e7278-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="e7278-114">**Unique Table**</span></span>
- <span data-ttu-id="e7278-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="e7278-115">**Update Resync**</span></span>
- <span data-ttu-id="e7278-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="e7278-116">**UpdateCriteria**</span></span>


<span data-ttu-id="e7278-p101">Essas propriedades são salvas na seção de esquema como atributos da definição do elemento do **Recordset** que está sendo mantido. Esses atributos são definidos no namespace do esquema do conjunto de linhas e deve ter o prefixo "rs:".</span><span class="sxs-lookup"><span data-stu-id="e7278-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="e7278-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7278-119">See also</span></span>

- [<span data-ttu-id="e7278-120">Propriedades dinâmicas do ADO</span><span class="sxs-lookup"><span data-stu-id="e7278-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
