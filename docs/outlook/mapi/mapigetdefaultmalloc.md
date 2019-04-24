---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345770"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="bb25e-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="bb25e-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="bb25e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb25e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb25e-105">Recupera o endereço da função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="bb25e-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb25e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bb25e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb25e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="bb25e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bb25e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bb25e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bb25e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bb25e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bb25e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="bb25e-110">Called by:</span></span>  <br/> |<span data-ttu-id="bb25e-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="bb25e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="bb25e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb25e-112">Parameters</span></span>

<span data-ttu-id="bb25e-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bb25e-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="bb25e-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bb25e-114">Return value</span></span>

<span data-ttu-id="bb25e-115">A função **MAPIGetDefaultMalloc** retorna um ponteiro para a função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="bb25e-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

