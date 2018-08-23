---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582032"
---
# <a name="checkparms"></a><span data-ttu-id="2dfea-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="2dfea-103">CheckParms</span></span>

  
  
<span data-ttu-id="2dfea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dfea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dfea-105">Chama uma função interna para validar os parâmetros de depuração em métodos do provedor de serviço chamados pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="2dfea-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2dfea-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2dfea-106">Header file:</span></span>  <br/> |<span data-ttu-id="2dfea-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2dfea-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2dfea-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="2dfea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2dfea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2dfea-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="2dfea-110">Called by:</span></span>  <br/> |<span data-ttu-id="2dfea-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2dfea-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="2dfea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dfea-112">Parameters</span></span>

 <span data-ttu-id="2dfea-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="2dfea-113">_eMethod_</span></span>
  
> <span data-ttu-id="2dfea-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="2dfea-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="2dfea-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="2dfea-115">_First_</span></span>
  
> <span data-ttu-id="2dfea-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="2dfea-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2dfea-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2dfea-117">Return value</span></span>

<span data-ttu-id="2dfea-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2dfea-118">S_OK</span></span> 
  
> <span data-ttu-id="2dfea-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2dfea-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2dfea-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dfea-120">Remarks</span></span>

<span data-ttu-id="2dfea-121">Ao contrário de macros [ValidateParms](validateparms.md) e [UlValidateParms](ulvalidateparms.md) , a macro **CheckParms** não realiza uma validação de parâmetro completo.</span><span class="sxs-lookup"><span data-stu-id="2dfea-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="2dfea-122">Parâmetros passados entre MAPI e o serviço provedores são consideradas corretas, portanto **CheckParms** executa apenas uma validação de depuração.</span><span class="sxs-lookup"><span data-stu-id="2dfea-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

