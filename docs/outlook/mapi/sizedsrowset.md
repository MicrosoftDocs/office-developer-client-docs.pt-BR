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
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282639"
---
# <a name="sizedsrowset"></a><span data-ttu-id="4379a-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="4379a-103">SizedSRowSet</span></span>

<span data-ttu-id="4379a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4379a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4379a-105">Cria uma estrutura nomeada do [SRowSet](srowset.md) que contém um número especificado de linhas.</span><span class="sxs-lookup"><span data-stu-id="4379a-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4379a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4379a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4379a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4379a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4379a-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="4379a-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4379a-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="4379a-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="4379a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4379a-110">Parameters</span></span>

<span data-ttu-id="4379a-111">__galinha_</span><span class="sxs-lookup"><span data-stu-id="4379a-111">__crow_</span></span>
  
> <span data-ttu-id="4379a-112">Contagem do número de linhas a serem incluídas na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="4379a-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="4379a-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="4379a-113">__name_</span></span>
  
> <span data-ttu-id="4379a-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="4379a-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4379a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4379a-115">Remarks</span></span>

<span data-ttu-id="4379a-116">Para usar a nova estrutura que resulta da macro **SizedSRowSet** como um ponteiro para uma estrutura **SRowSet** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="4379a-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="4379a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4379a-117">See also</span></span>

- [<span data-ttu-id="4379a-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4379a-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="4379a-119">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="4379a-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

