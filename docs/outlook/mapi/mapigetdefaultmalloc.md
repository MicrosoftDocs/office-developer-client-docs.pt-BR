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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592329"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="aff2d-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="aff2d-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="aff2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aff2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aff2d-105">Recupera o endereço da função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="aff2d-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aff2d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="aff2d-106">Header file:</span></span>  <br/> |<span data-ttu-id="aff2d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="aff2d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="aff2d-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="aff2d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aff2d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aff2d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aff2d-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="aff2d-110">Called by:</span></span>  <br/> |<span data-ttu-id="aff2d-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="aff2d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="aff2d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aff2d-112">Parameters</span></span>

<span data-ttu-id="aff2d-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="aff2d-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="aff2d-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aff2d-114">Return value</span></span>

<span data-ttu-id="aff2d-115">A função **MAPIGetDefaultMalloc** retorna um ponteiro para a função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="aff2d-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

