---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567052"
---
# <a name="checkparameters"></a><span data-ttu-id="fc956-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="fc956-103">CheckParameters</span></span>

  
  
<span data-ttu-id="fc956-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc956-105">Chama uma função interna para validar os parâmetros de depuração em métodos do provedor de serviço chamados pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="fc956-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc956-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fc956-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc956-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="fc956-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="fc956-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="fc956-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc956-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc956-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc956-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="fc956-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc956-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="fc956-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="fc956-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc956-112">Parameters</span></span>

 <span data-ttu-id="fc956-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="fc956-113">_eMethod_</span></span>
  
> <span data-ttu-id="fc956-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="fc956-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="fc956-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="fc956-115">_First_</span></span>
  
> <span data-ttu-id="fc956-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="fc956-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc956-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fc956-117">Return value</span></span>

<span data-ttu-id="fc956-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc956-118">S_OK</span></span> 
  
> <span data-ttu-id="fc956-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fc956-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc956-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc956-120">Remarks</span></span>

<span data-ttu-id="fc956-121">A macro **CheckParameters** foi substituída pela macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="fc956-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="fc956-122">**CheckParms** é recomendável em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="fc956-122">**CheckParms** is recommended on all platforms.</span></span> 
  

