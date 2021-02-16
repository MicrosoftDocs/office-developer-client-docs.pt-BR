---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423381"
---
# <a name="ftnegft"></a><span data-ttu-id="2b6c5-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="2b6c5-103">FtNegFt</span></span>

  
  
<span data-ttu-id="2b6c5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b6c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b6c5-105">Calcula o complemento dos dois de um inteiro de 64 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="2b6c5-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b6c5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2b6c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b6c5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2b6c5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2b6c5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2b6c5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2b6c5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2b6c5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2b6c5-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2b6c5-110">Called by:</span></span>  <br/> |<span data-ttu-id="2b6c5-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2b6c5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="2b6c5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b6c5-112">Parameters</span></span>

 <span data-ttu-id="2b6c5-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="2b6c5-113">_ft_</span></span>
  
> <span data-ttu-id="2b6c5-114">[in] Uma [estrutura FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado para o qual calcular o complemento dos dois.</span><span class="sxs-lookup"><span data-stu-id="2b6c5-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2b6c5-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2b6c5-115">Return value</span></span>

<span data-ttu-id="2b6c5-116">A **função FtNegFt** retorna uma estrutura **FILETIME** que contém o complemento dos dois números inteiros.</span><span class="sxs-lookup"><span data-stu-id="2b6c5-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="2b6c5-117">O parâmetro de entrada permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="2b6c5-117">The input parameter remains unchanged.</span></span> 
  

