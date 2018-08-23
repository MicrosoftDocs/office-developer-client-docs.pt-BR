---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583936"
---
# <a name="sizedsrowset"></a><span data-ttu-id="36473-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="36473-103">SizedSRowSet</span></span>

<span data-ttu-id="36473-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36473-105">Cria uma estrutura [SRowSet](srowset.md) nomeada que contém um número especificado de linhas.</span><span class="sxs-lookup"><span data-stu-id="36473-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36473-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="36473-106">Header file:</span></span>  <br/> |<span data-ttu-id="36473-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36473-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="36473-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="36473-108">Related structure:</span></span>  <br/> |<span data-ttu-id="36473-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="36473-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="36473-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36473-110">Parameters</span></span>

<span data-ttu-id="36473-111">__galinha_</span><span class="sxs-lookup"><span data-stu-id="36473-111">__crow_</span></span>
  
> <span data-ttu-id="36473-112">Contagem do número de linhas a serem incluídos na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="36473-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="36473-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="36473-113">__name_</span></span>
  
> <span data-ttu-id="36473-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="36473-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36473-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="36473-115">Remarks</span></span>

<span data-ttu-id="36473-116">Para usar a nova estrutura que é resultado da macro **SizedSRowSet** como um ponteiro para uma estrutura **SRowSet** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="36473-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="36473-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="36473-117">See also</span></span>

- [<span data-ttu-id="36473-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="36473-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="36473-119">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="36473-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

