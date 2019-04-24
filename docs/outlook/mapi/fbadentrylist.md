---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341066"
---
# <a name="fbadentrylist"></a><span data-ttu-id="9f930-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="9f930-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="9f930-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f930-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f930-105">Valida uma lista de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f930-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f930-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9f930-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f930-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9f930-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9f930-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9f930-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f930-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f930-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f930-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9f930-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f930-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9f930-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="9f930-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f930-112">Parameters</span></span>

 <span data-ttu-id="9f930-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="9f930-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="9f930-114">no Ponteiro para uma [](entrylist.md) estrutura ENTRYLIST que contém uma matriz de identificadores de entrada a ser validada.</span><span class="sxs-lookup"><span data-stu-id="9f930-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f930-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f930-115">Return value</span></span>

<span data-ttu-id="9f930-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f930-116">TRUE</span></span> 
  
> <span data-ttu-id="9f930-117">Um ou mais dos identificadores de entrada listados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="9f930-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="9f930-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="9f930-118">FALSE</span></span> 
  
> <span data-ttu-id="9f930-119">Todos os identificadores de entrada listados são válidos.</span><span class="sxs-lookup"><span data-stu-id="9f930-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f930-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f930-120">Remarks</span></span>

<span data-ttu-id="9f930-121">A função **FBadEntryList** determina se a lista de identificadores de entrada foi gerada corretamente.</span><span class="sxs-lookup"><span data-stu-id="9f930-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="9f930-122">Um exemplo de um identificador inválido é aquele para o qual a memória foi alocada incorretamente ou um identificador de tamanho incorreto.</span><span class="sxs-lookup"><span data-stu-id="9f930-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

