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
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433392"
---
# <a name="checkparameters"></a><span data-ttu-id="f9c6c-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="f9c6c-103">CheckParameters</span></span>

  
  
<span data-ttu-id="f9c6c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9c6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9c6c-105">Chama uma função interna para validar parâmetros de depuração em métodos de provedor de serviços chamados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9c6c-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9c6c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f9c6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9c6c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f9c6c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f9c6c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f9c6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9c6c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9c6c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9c6c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f9c6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9c6c-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="f9c6c-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f9c6c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9c6c-112">Parameters</span></span>

 <span data-ttu-id="f9c6c-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f9c6c-113">_eMethod_</span></span>
  
> <span data-ttu-id="f9c6c-114">[in] Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="f9c6c-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f9c6c-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="f9c6c-115">_First_</span></span>
  
> <span data-ttu-id="f9c6c-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="f9c6c-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9c6c-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f9c6c-117">Return value</span></span>

<span data-ttu-id="f9c6c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9c6c-118">S_OK</span></span> 
  
> <span data-ttu-id="f9c6c-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f9c6c-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9c6c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9c6c-120">Remarks</span></span>

<span data-ttu-id="f9c6c-121">A **macro CheckParameters** foi sobressalvada pela macro [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="f9c6c-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="f9c6c-122">**CheckParms é** recomendado em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="f9c6c-122">**CheckParms** is recommended on all platforms.</span></span> 
  

