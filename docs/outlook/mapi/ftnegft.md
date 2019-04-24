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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327969"
---
# <a name="ftnegft"></a><span data-ttu-id="9af43-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="9af43-103">FtNegFt</span></span>

  
  
<span data-ttu-id="9af43-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9af43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9af43-105">Computa o complemento de um inteiro de 64 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="9af43-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9af43-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9af43-106">Header file:</span></span>  <br/> |<span data-ttu-id="9af43-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="9af43-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9af43-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9af43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9af43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9af43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9af43-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9af43-110">Called by:</span></span>  <br/> |<span data-ttu-id="9af43-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9af43-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="9af43-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9af43-112">Parameters</span></span>

 <span data-ttu-id="9af43-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="9af43-113">_ft_</span></span>
  
> <span data-ttu-id="9af43-114">no Uma estrutura [FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado para o qual calcular o complemento de dois.</span><span class="sxs-lookup"><span data-stu-id="9af43-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9af43-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9af43-115">Return value</span></span>

<span data-ttu-id="9af43-116">A função **FtNegFt** retorna uma estrutura **FILETIME** que contém o complemento de dois do inteiro.</span><span class="sxs-lookup"><span data-stu-id="9af43-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="9af43-117">O parâmetro de entrada permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="9af43-117">The input parameter remains unchanged.</span></span> 
  

