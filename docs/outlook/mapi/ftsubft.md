---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766638"
---
# <a name="ftsubft"></a><span data-ttu-id="c5a9c-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="c5a9c-103">FtSubFt</span></span>

  
  
<span data-ttu-id="c5a9c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5a9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5a9c-105">Subtrai um inteiro não assinado de 64 bits do outro.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5a9c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c5a9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5a9c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c5a9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c5a9c-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c5a9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5a9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5a9c-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c5a9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c5a9c-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c5a9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="c5a9c-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c5a9c-112">Parameters</span></span>

 <span data-ttu-id="c5a9c-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="c5a9c-113">_Minuend_</span></span>
  
> <span data-ttu-id="c5a9c-114">[in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits do qual o valor no parâmetro _Subtrahend_ deve ser subtraídos.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="c5a9c-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="c5a9c-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="c5a9c-116">[in] Uma estrutura **FILETIME** que contém o inteiro não assinado de 64 bits é subtraído do valor indicado pelo parâmetro _Minuend_ .</span><span class="sxs-lookup"><span data-stu-id="c5a9c-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5a9c-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c5a9c-117">Return value</span></span>

<span data-ttu-id="c5a9c-118">A função **FtSubFt** retorna uma estrutura **FILETIME** que contém o resultado de subtração.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="c5a9c-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="c5a9c-119">The two input parameters remain unchanged.</span></span> 
  

