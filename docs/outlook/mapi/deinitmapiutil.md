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
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427343"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="86daf-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="86daf-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="86daf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86daf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86daf-105">Libera funções de utilitário chamadas explicitamente pela função [ScInitMapiUtil](scinitmapiutil.md) ou implicitamente pela [função MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="86daf-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86daf-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="86daf-106">Header file:</span></span>  <br/> |<span data-ttu-id="86daf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="86daf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="86daf-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="86daf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86daf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="86daf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="86daf-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="86daf-110">Called by:</span></span>  <br/> |<span data-ttu-id="86daf-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="86daf-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="86daf-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86daf-112">Parameters</span></span>

<span data-ttu-id="86daf-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="86daf-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="86daf-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86daf-114">Return value</span></span>

<span data-ttu-id="86daf-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="86daf-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86daf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="86daf-116">Remarks</span></span>

<span data-ttu-id="86daf-117">As **funções de lançamento DeinitMapiUtil** inicializadas com [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="86daf-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="86daf-118">Quando o uso das funções chamadas por **ScInitMapiUtil** for concluído, **DeinitMapiUtil** deverá ser chamado explicitamente para liberá-las.</span><span class="sxs-lookup"><span data-stu-id="86daf-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="86daf-119">Por outro lado, [MAPIUninitialize](mapiuninitialize.md) implicitamente chama **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="86daf-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

