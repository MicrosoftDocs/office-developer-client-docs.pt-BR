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
# <a name="checkparms"></a><span data-ttu-id="191b8-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="191b8-103">CheckParms</span></span>

  
  
<span data-ttu-id="191b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="191b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="191b8-105">Chama uma função interna para validar parâmetros de depuração nos métodos de provedor de serviços chamados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="191b8-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="191b8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="191b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="191b8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="191b8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="191b8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="191b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="191b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="191b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="191b8-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="191b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="191b8-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="191b8-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="191b8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="191b8-112">Parameters</span></span>

 <span data-ttu-id="191b8-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="191b8-113">_eMethod_</span></span>
  
> <span data-ttu-id="191b8-114">no Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="191b8-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="191b8-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="191b8-115">_First_</span></span>
  
> <span data-ttu-id="191b8-116">no Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="191b8-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="191b8-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="191b8-117">Return value</span></span>

<span data-ttu-id="191b8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="191b8-118">S_OK</span></span> 
  
> <span data-ttu-id="191b8-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="191b8-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="191b8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="191b8-120">Remarks</span></span>

<span data-ttu-id="191b8-121">Ao contrário das macros [ValidateParms](validateparms.md) e [UlValidateParms](ulvalidateparms.md) , a macro **CheckParms** não realiza uma validação de parâmetro completa.</span><span class="sxs-lookup"><span data-stu-id="191b8-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="191b8-122">Os parâmetros passados entre MAPI e provedores de serviço são considerados corretos, portanto, **CheckParms** executa apenas uma validação de depuração.</span><span class="sxs-lookup"><span data-stu-id="191b8-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

