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
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589235"
---
# <a name="ftnegft"></a><span data-ttu-id="0e1ad-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="0e1ad-103">FtNegFt</span></span>

  
  
<span data-ttu-id="0e1ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e1ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e1ad-105">Computa das duas complemento de um inteiro não assinado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e1ad-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0e1ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e1ad-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0e1ad-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0e1ad-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0e1ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e1ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e1ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e1ad-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0e1ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e1ad-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0e1ad-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="0e1ad-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e1ad-112">Parameters</span></span>

 <span data-ttu-id="0e1ad-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="0e1ad-113">_ft_</span></span>
  
> <span data-ttu-id="0e1ad-114">[in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits para a qual calcular das duas complemento.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e1ad-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0e1ad-115">Return value</span></span>

<span data-ttu-id="0e1ad-116">A função **FtNegFt** retorna uma estrutura **FILETIME** que contém das duas complemento do inteiro.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="0e1ad-117">O parâmetro de entrada permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-117">The input parameter remains unchanged.</span></span> 
  

