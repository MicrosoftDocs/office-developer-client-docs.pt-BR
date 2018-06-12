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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766535"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="eaf02-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="eaf02-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="eaf02-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eaf02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eaf02-105">Os testes a validade de uma coluna de tabela definida para usam por um provedor de serviço em uma chamada subsequente ao método [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf02-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eaf02-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eaf02-106">Header file:</span></span>  <br/> |<span data-ttu-id="eaf02-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="eaf02-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="eaf02-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="eaf02-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eaf02-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eaf02-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eaf02-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="eaf02-110">Called by:</span></span>  <br/> |<span data-ttu-id="eaf02-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="eaf02-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="eaf02-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="eaf02-112">Parameters</span></span>

 <span data-ttu-id="eaf02-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="eaf02-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="eaf02-114">[in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade definindo as colunas da tabela para validar.</span><span class="sxs-lookup"><span data-stu-id="eaf02-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eaf02-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eaf02-115">Return value</span></span>

<span data-ttu-id="eaf02-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="eaf02-116">TRUE</span></span> 
  
> <span data-ttu-id="eaf02-117">O conjunto de coluna especificada é inválido.</span><span class="sxs-lookup"><span data-stu-id="eaf02-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="eaf02-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="eaf02-118">FALSE</span></span> 
  
> <span data-ttu-id="eaf02-119">O conjunto de coluna especificada é válido.</span><span class="sxs-lookup"><span data-stu-id="eaf02-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaf02-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="eaf02-120">Remarks</span></span>

<span data-ttu-id="eaf02-121">A função **FBadColumnSet** trata as colunas do tipo PT_ERROR como inválida e colunas do tipo PT_NULL como válido.</span><span class="sxs-lookup"><span data-stu-id="eaf02-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

