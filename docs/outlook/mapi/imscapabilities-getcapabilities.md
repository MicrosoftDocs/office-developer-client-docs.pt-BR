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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317434"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="cff12-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="cff12-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="cff12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cff12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cff12-105">Obtém informações sobre o que um repositório pode suportar com base no seletor especificado.</span><span class="sxs-lookup"><span data-stu-id="cff12-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="cff12-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cff12-106">Parameters</span></span>

 <span data-ttu-id="cff12-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="cff12-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="cff12-108">no Seletor que indica quais recursos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="cff12-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cff12-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cff12-109">Return value</span></span>

<span data-ttu-id="cff12-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="cff12-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="cff12-111">Suporte para home pages de pastas em um repositório não padrão.</span><span class="sxs-lookup"><span data-stu-id="cff12-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="cff12-112">Isso pode ser retornado se **MSCAP_SEL_FOLDER** for especificado em *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="cff12-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="cff12-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="cff12-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="cff12-114">Se uma restrição contiver argumentos inválidos como propriedades inválidas, o repositório ignorará os argumentos inválidos e processará apenas os argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="cff12-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="cff12-115">Isso pode ser retornado se **MSCAP_SEL_RESTRICTION** for especificado em *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="cff12-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="cff12-116">VAZIO</span><span class="sxs-lookup"><span data-stu-id="cff12-116">NULL</span></span>
  
> <span data-ttu-id="cff12-117">O repositório não dá suporte a qualquer recurso com base no seletor especificado.</span><span class="sxs-lookup"><span data-stu-id="cff12-117">The store does not support any capability based on the given selector.</span></span>
    

