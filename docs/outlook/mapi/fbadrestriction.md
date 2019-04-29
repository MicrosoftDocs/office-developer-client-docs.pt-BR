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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432237"
---
# <a name="fbadrestriction"></a><span data-ttu-id="05579-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="05579-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="05579-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05579-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05579-105">Valida uma restrição usada para limitar um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="05579-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05579-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="05579-106">Header file:</span></span>  <br/> |<span data-ttu-id="05579-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="05579-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="05579-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="05579-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="05579-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="05579-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="05579-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="05579-110">Called by:</span></span>  <br/> |<span data-ttu-id="05579-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="05579-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="05579-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05579-112">Parameters</span></span>

 <span data-ttu-id="05579-113">_lpRes_</span><span class="sxs-lookup"><span data-stu-id="05579-113">_lpres_</span></span>
  
> <span data-ttu-id="05579-114">no Uma estrutura [SRestriction](srestriction.md) que define a restrição a ser validada.</span><span class="sxs-lookup"><span data-stu-id="05579-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05579-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05579-115">Return value</span></span>

<span data-ttu-id="05579-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="05579-116">TRUE</span></span> 
  
> <span data-ttu-id="05579-117">A restrição especificada, ou uma ou mais de suas subrestrições, é inválida.</span><span class="sxs-lookup"><span data-stu-id="05579-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="05579-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="05579-118">FALSE</span></span> 
  
> <span data-ttu-id="05579-119">A restrição especificada e todas as suas subrestriçãos são válidas.</span><span class="sxs-lookup"><span data-stu-id="05579-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05579-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="05579-120">Remarks</span></span>

<span data-ttu-id="05579-121">Depois que uma restrição é validada, ela pode ser transmitida em chamadas para o método imApitable [:: Restrict](imapitable-restrict.md) para restringir a tabela a determinadas linhas, para o método IMAPITable: [: FindRow](imapitable-findrow.md) para localizar uma linha de tabela e para métodos do [IMAPIContainer](imapicontainerimapiprop.md) interface para executar uma restrição em um objeto Container.</span><span class="sxs-lookup"><span data-stu-id="05579-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

