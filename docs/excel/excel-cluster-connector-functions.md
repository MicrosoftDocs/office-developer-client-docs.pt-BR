---
title: Funções do conector de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408583"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="da01d-103">Funções do conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="da01d-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="da01d-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da01d-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="da01d-105">As DLLs do conector de cluster do Microsoft Excel 2013 devem implementar as funções descritas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="da01d-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="da01d-106">Os valores de retorno mencionados nos tópicos de referência nesta seção são definidos no arquivo de inclusão do SDK, xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="da01d-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="da01d-107">Arquitetura do conector de cluster</span><span class="sxs-lookup"><span data-stu-id="da01d-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="da01d-108">O Excel chama pontos de entrada em um conector de cluster para transferir chamadas de função definidas pelo usuário para um cluster de computação de alto desempenho e para gerenciamento de sessão de cluster.</span><span class="sxs-lookup"><span data-stu-id="da01d-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="da01d-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="da01d-109">In this section</span></span>

[<span data-ttu-id="da01d-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="da01d-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="da01d-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="da01d-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="da01d-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="da01d-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="da01d-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="da01d-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="da01d-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="da01d-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="da01d-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="da01d-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="da01d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="da01d-116">See also</span></span>



[<span data-ttu-id="da01d-117">Developing Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="da01d-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="da01d-118">Funções seguras para clusters</span><span class="sxs-lookup"><span data-stu-id="da01d-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

