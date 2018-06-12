---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766532"
---
# <a name="fbadrestriction"></a><span data-ttu-id="6f278-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="6f278-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="6f278-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f278-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f278-105">Valida uma restrição usada para limitar a um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="6f278-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f278-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6f278-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f278-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6f278-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6f278-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="6f278-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f278-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f278-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6f278-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="6f278-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f278-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6f278-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="6f278-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6f278-112">Parameters</span></span>

 <span data-ttu-id="6f278-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="6f278-113">_lpres_</span></span>
  
> <span data-ttu-id="6f278-114">[in] Uma estrutura de [SRestriction](srestriction.md) definindo a restrição a ser validado.</span><span class="sxs-lookup"><span data-stu-id="6f278-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f278-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6f278-115">Return value</span></span>

<span data-ttu-id="6f278-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="6f278-116">TRUE</span></span> 
  
> <span data-ttu-id="6f278-117">A restrição especificada, ou uma ou mais das suas subrestrictions, são inválido.</span><span class="sxs-lookup"><span data-stu-id="6f278-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="6f278-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="6f278-118">FALSE</span></span> 
  
> <span data-ttu-id="6f278-119">A restrição especificada e todos os seus subrestrictions são válidos.</span><span class="sxs-lookup"><span data-stu-id="6f278-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f278-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6f278-120">Remarks</span></span>

<span data-ttu-id="6f278-121">Depois que uma restrição é validada, ela poderá ser passada em chamadas para o método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir a tabela para determinadas linhas, para o método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha da tabela e para os métodos do [IMAPIContainer](imapicontainerimapiprop.md) interface para realizar uma restrição em um objeto container.</span><span class="sxs-lookup"><span data-stu-id="6f278-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

