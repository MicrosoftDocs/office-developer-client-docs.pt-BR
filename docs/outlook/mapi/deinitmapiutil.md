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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336838"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="10ce5-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="10ce5-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="10ce5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10ce5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10ce5-105">Libera funções utilitárias chamadas explicitamente pela função [ScInitMapiUtil](scinitmapiutil.md) ou implicitamente pela função [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="10ce5-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10ce5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="10ce5-106">Header file:</span></span>  <br/> |<span data-ttu-id="10ce5-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="10ce5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="10ce5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="10ce5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="10ce5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="10ce5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="10ce5-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="10ce5-110">Called by:</span></span>  <br/> |<span data-ttu-id="10ce5-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="10ce5-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="10ce5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10ce5-112">Parameters</span></span>

<span data-ttu-id="10ce5-113">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="10ce5-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="10ce5-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="10ce5-114">Return value</span></span>

<span data-ttu-id="10ce5-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10ce5-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10ce5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10ce5-116">Remarks</span></span>

<span data-ttu-id="10ce5-117">As funções de lançamento da função **DeinitMapiUtil** inicializadas com o [ScInitMapiUtil](scinitmapiutil.md) ou o [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="10ce5-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="10ce5-118">Quando o uso das funções chamadas por **ScInitMapiUtil** estiver concluído, **DeinitMapiUtil** deverá ser explicitamente chamado para liberá-las.</span><span class="sxs-lookup"><span data-stu-id="10ce5-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="10ce5-119">Por outro lado, [MAPIUninitialize](mapiuninitialize.md) chama implicitamente **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="10ce5-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

