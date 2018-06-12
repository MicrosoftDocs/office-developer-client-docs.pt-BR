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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766283"
---
# <a name="checkparms"></a><span data-ttu-id="fb9bd-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="fb9bd-103">CheckParms</span></span>

  
  
<span data-ttu-id="fb9bd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb9bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb9bd-105">Chama uma função interna para validar os parâmetros de depuração em métodos do provedor de serviço chamados pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb9bd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fb9bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb9bd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="fb9bd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="fb9bd-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="fb9bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fb9bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fb9bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fb9bd-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="fb9bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="fb9bd-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="fb9bd-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="fb9bd-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="fb9bd-112">Parameters</span></span>

 <span data-ttu-id="fb9bd-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="fb9bd-113">_eMethod_</span></span>
  
> <span data-ttu-id="fb9bd-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="fb9bd-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="fb9bd-115">_First_</span></span>
  
> <span data-ttu-id="fb9bd-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb9bd-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fb9bd-117">Return value</span></span>

<span data-ttu-id="fb9bd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb9bd-118">S_OK</span></span> 
  
> <span data-ttu-id="fb9bd-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb9bd-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="fb9bd-120">Remarks</span></span>

<span data-ttu-id="fb9bd-121">Ao contrário de macros [ValidateParms](validateparms.md) e [UlValidateParms](ulvalidateparms.md) , a macro **CheckParms** não realiza uma validação de parâmetro completo.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="fb9bd-122">Parâmetros passados entre MAPI e o serviço provedores são consideradas corretas, portanto **CheckParms** executa apenas uma validação de depuração.</span><span class="sxs-lookup"><span data-stu-id="fb9bd-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

