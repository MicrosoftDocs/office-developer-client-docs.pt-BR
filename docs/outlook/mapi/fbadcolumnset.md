---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434715"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="9a6b1-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="9a6b1-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="9a6b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a6b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a6b1-105">Testa a validade de uma coluna de tabela definida para uso por um provedor de serviços em uma chamada subsequente para o método [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="9a6b1-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a6b1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9a6b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a6b1-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9a6b1-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9a6b1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9a6b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a6b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9a6b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9a6b1-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9a6b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="9a6b1-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9a6b1-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="9a6b1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a6b1-112">Parameters</span></span>

 <span data-ttu-id="9a6b1-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="9a6b1-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="9a6b1-114">[in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade definindo as colunas da tabela a validar.</span><span class="sxs-lookup"><span data-stu-id="9a6b1-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a6b1-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9a6b1-115">Return value</span></span>

<span data-ttu-id="9a6b1-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a6b1-116">TRUE</span></span> 
  
> <span data-ttu-id="9a6b1-117">O conjunto de colunas especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="9a6b1-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="9a6b1-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a6b1-118">FALSE</span></span> 
  
> <span data-ttu-id="9a6b1-119">O conjunto de colunas especificado é válido.</span><span class="sxs-lookup"><span data-stu-id="9a6b1-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a6b1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a6b1-120">Remarks</span></span>

<span data-ttu-id="9a6b1-121">A **função FBadColumnSet** trata colunas do tipo PT_ERROR como inválidas e colunas do tipo PT_NULL como válidas.</span><span class="sxs-lookup"><span data-stu-id="9a6b1-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

