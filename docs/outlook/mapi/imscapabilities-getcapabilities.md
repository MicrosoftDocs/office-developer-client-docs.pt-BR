---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767478"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="f8d5a-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="f8d5a-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="f8d5a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8d5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8d5a-105">Obtém informações sobre o que pode suportar um repositório com base no seletor especificado.</span><span class="sxs-lookup"><span data-stu-id="f8d5a-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="f8d5a-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f8d5a-106">Parameters</span></span>

 <span data-ttu-id="f8d5a-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="f8d5a-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="f8d5a-108">[in] Seletor indicando quais recursos para retornar.</span><span class="sxs-lookup"><span data-stu-id="f8d5a-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8d5a-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8d5a-109">Return value</span></span>

<span data-ttu-id="f8d5a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="f8d5a-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="f8d5a-111">Suporte para home pages de pasta em um repositório não padrão.</span><span class="sxs-lookup"><span data-stu-id="f8d5a-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="f8d5a-112">Isso pode ser retornado se **MSCAP_SEL_FOLDER** for especificado no *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="f8d5a-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="f8d5a-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="f8d5a-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="f8d5a-114">Se uma restrição contiver nenhum argumento inválido como propriedades inválidos, o repositório ignora os argumentos inválidos e processa somente os argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="f8d5a-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="f8d5a-115">Isso pode ser retornado se **MSCAP_SEL_RESTRICTION** for especificado no *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="f8d5a-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="f8d5a-116">NULL</span><span class="sxs-lookup"><span data-stu-id="f8d5a-116">NULL</span></span>
  
> <span data-ttu-id="f8d5a-117">O repositório não oferece suporte a qualquer recurso com base no seletor determinado.</span><span class="sxs-lookup"><span data-stu-id="f8d5a-117">The store does not support any capability based on the given selector.</span></span>
    

