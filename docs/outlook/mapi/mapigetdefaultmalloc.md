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
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767982"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="dfc24-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="dfc24-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="dfc24-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfc24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfc24-105">Recupera o endereço da função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="dfc24-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc24-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dfc24-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfc24-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dfc24-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dfc24-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="dfc24-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfc24-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc24-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dfc24-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="dfc24-110">Called by:</span></span>  <br/> |<span data-ttu-id="dfc24-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="dfc24-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="dfc24-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc24-112">Parameters</span></span>

<span data-ttu-id="dfc24-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="dfc24-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="dfc24-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dfc24-114">Return value</span></span>

<span data-ttu-id="dfc24-115">A função **MAPIGetDefaultMalloc** retorna um ponteiro para a função de alocação de memória MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="dfc24-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

