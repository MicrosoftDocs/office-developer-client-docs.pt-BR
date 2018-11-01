---
title: Propriedades dinâmicas do recordset em XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884258"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="992d0-102">Propriedades dinâmicas do recordset em XML</span><span class="sxs-lookup"><span data-stu-id="992d0-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="992d0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="992d0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="992d0-104">Propriedades dinâmicas do recordset em XML</span><span class="sxs-lookup"><span data-stu-id="992d0-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="992d0-105">As propriedades específicas do provedor do **Recordset** a seguir (do Mecanismo de cursor do cliente) são mantidas atualmente no formato XML:</span><span class="sxs-lookup"><span data-stu-id="992d0-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="992d0-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="992d0-106">**Update Resync**</span></span>

  - <span data-ttu-id="992d0-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="992d0-107">**Unique Table**</span></span>

  - <span data-ttu-id="992d0-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="992d0-108">**Unique Schema**</span></span>

  - <span data-ttu-id="992d0-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="992d0-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="992d0-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="992d0-110">**Resync Command**</span></span>

  - <span data-ttu-id="992d0-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="992d0-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="992d0-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="992d0-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="992d0-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="992d0-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="992d0-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="992d0-114">**BatchSize**</span></span>

  - <span data-ttu-id="992d0-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="992d0-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="992d0-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="992d0-116">**Reshape Name**</span></span>

  - <span data-ttu-id="992d0-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="992d0-117">**AutoRecalc**</span></span>

<span data-ttu-id="992d0-p101">Essas propriedades são salvas na seção de esquema como atributos da definição do elemento do **Recordset** que está sendo mantido. Esses atributos são definidos no namespace do esquema do conjunto de linhas e deve ter o prefixo "rs:".</span><span class="sxs-lookup"><span data-stu-id="992d0-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

