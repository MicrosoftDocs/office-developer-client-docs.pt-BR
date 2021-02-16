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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409255"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="ad389-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ad389-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="ad389-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad389-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad389-105">Obtém informações sobre o que um armazenamento pode suportar com base no seletor especificado.</span><span class="sxs-lookup"><span data-stu-id="ad389-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="ad389-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad389-106">Parameters</span></span>

 <span data-ttu-id="ad389-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="ad389-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="ad389-108">[in] Seletor indicando quais recursos retornar.</span><span class="sxs-lookup"><span data-stu-id="ad389-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad389-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad389-109">Return value</span></span>

<span data-ttu-id="ad389-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="ad389-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="ad389-111">Suporte para homepages de pasta em um armazenamento não padrão.</span><span class="sxs-lookup"><span data-stu-id="ad389-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="ad389-112">Isso pode ser retornado **se MSCAP_SEL_FOLDER** especificado em  *mscapSelector*  .</span><span class="sxs-lookup"><span data-stu-id="ad389-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="ad389-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="ad389-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="ad389-114">Se uma restrição contiver argumentos inválidos, como propriedades inválidas, o armazenamento ignorará os argumentos inválidos e processa apenas os argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="ad389-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="ad389-115">Isso pode ser retornado **se MSCAP_SEL_RESTRICTION** especificado em  *mscapSelector*  .</span><span class="sxs-lookup"><span data-stu-id="ad389-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="ad389-116">NULL</span><span class="sxs-lookup"><span data-stu-id="ad389-116">NULL</span></span>
  
> <span data-ttu-id="ad389-117">O armazenamento não dá suporte a nenhum recurso com base no seletor determinado.</span><span class="sxs-lookup"><span data-stu-id="ad389-117">The store does not support any capability based on the given selector.</span></span>
    

