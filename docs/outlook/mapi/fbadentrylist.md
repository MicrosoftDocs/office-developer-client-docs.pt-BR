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
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766521"
---
# <a name="fbadentrylist"></a><span data-ttu-id="99d70-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="99d70-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="99d70-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99d70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99d70-105">Valida uma lista dos identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="99d70-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99d70-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="99d70-106">Header file:</span></span>  <br/> |<span data-ttu-id="99d70-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="99d70-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="99d70-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="99d70-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="99d70-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="99d70-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="99d70-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="99d70-110">Called by:</span></span>  <br/> |<span data-ttu-id="99d70-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="99d70-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="99d70-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99d70-112">Parameters</span></span>

 <span data-ttu-id="99d70-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="99d70-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="99d70-114">[in] Ponteiro para uma estrutura [ENTRYLIST](entrylist.md) que contém uma matriz de identificadores de entrada a ser validado.</span><span class="sxs-lookup"><span data-stu-id="99d70-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99d70-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="99d70-115">Return value</span></span>

<span data-ttu-id="99d70-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="99d70-116">TRUE</span></span> 
  
> <span data-ttu-id="99d70-117">Um ou mais dos identificadores de entrada listada são inválidos.</span><span class="sxs-lookup"><span data-stu-id="99d70-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="99d70-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="99d70-118">FALSE</span></span> 
  
> <span data-ttu-id="99d70-119">Todos os identificadores de entrada listada são válidos.</span><span class="sxs-lookup"><span data-stu-id="99d70-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99d70-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="99d70-120">Remarks</span></span>

<span data-ttu-id="99d70-121">A função **FBadEntryList** determina se a lista de identificadores de entrada foi gerada corretamente.</span><span class="sxs-lookup"><span data-stu-id="99d70-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="99d70-122">Um exemplo de um identificador inválido é aquele para o qual memória foi alocada incorretamente ou um identificador de um tamanho incorreto.</span><span class="sxs-lookup"><span data-stu-id="99d70-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

