---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574794"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="01787-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="01787-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="01787-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01787-105">Libera funções do utilitário chamadas explicitamente pela função [ScInitMapiUtil](scinitmapiutil.md) ou implicitamente pela função [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="01787-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01787-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="01787-106">Header file:</span></span>  <br/> |<span data-ttu-id="01787-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01787-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01787-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="01787-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01787-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01787-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01787-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="01787-110">Called by:</span></span>  <br/> |<span data-ttu-id="01787-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="01787-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="01787-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01787-112">Parameters</span></span>

<span data-ttu-id="01787-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="01787-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="01787-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="01787-114">Return value</span></span>

<span data-ttu-id="01787-115">None</span><span class="sxs-lookup"><span data-stu-id="01787-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01787-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="01787-116">Remarks</span></span>

<span data-ttu-id="01787-117">A função **DeinitMapiUtil** release funções inicializadas com [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="01787-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="01787-118">Quando o uso das funções chamado pelo **ScInitMapiUtil** estiver concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-los.</span><span class="sxs-lookup"><span data-stu-id="01787-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="01787-119">Por outro lado, [MAPIUninitialize](mapiuninitialize.md) implicitamente chama **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="01787-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

