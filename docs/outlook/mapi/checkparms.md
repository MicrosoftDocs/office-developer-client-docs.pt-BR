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
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422275"
---
# <a name="checkparms"></a><span data-ttu-id="7d802-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="7d802-103">CheckParms</span></span>

  
  
<span data-ttu-id="7d802-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d802-105">Chama uma função interna para validar parâmetros de depuração em métodos de provedor de serviços chamados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d802-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d802-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7d802-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d802-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7d802-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7d802-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7d802-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7d802-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7d802-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7d802-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="7d802-110">Called by:</span></span>  <br/> |<span data-ttu-id="7d802-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="7d802-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="7d802-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d802-112">Parameters</span></span>

 <span data-ttu-id="7d802-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="7d802-113">_eMethod_</span></span>
  
> <span data-ttu-id="7d802-114">[in] Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="7d802-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="7d802-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="7d802-115">_First_</span></span>
  
> <span data-ttu-id="7d802-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="7d802-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d802-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7d802-117">Return value</span></span>

<span data-ttu-id="7d802-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d802-118">S_OK</span></span> 
  
> <span data-ttu-id="7d802-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7d802-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d802-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d802-120">Remarks</span></span>

<span data-ttu-id="7d802-121">Ao contrário das macros [ValidateParms](validateparms.md) e [UlValidateParms,](ulvalidateparms.md) a macro **CheckParms** não executa uma validação de parâmetro completa.</span><span class="sxs-lookup"><span data-stu-id="7d802-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="7d802-122">Os parâmetros passados entre o MAPI e os provedores de serviços são assumidos como corretos, portanto, **CheckParms** executa apenas uma validação de depuração.</span><span class="sxs-lookup"><span data-stu-id="7d802-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

