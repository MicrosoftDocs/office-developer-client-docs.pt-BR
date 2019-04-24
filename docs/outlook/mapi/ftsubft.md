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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300389"
---
# <a name="ftsubft"></a><span data-ttu-id="023dc-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="023dc-103">FtSubFt</span></span>

  
  
<span data-ttu-id="023dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="023dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="023dc-105">Subtrai um inteiro de 64 bits não assinado de outro.</span><span class="sxs-lookup"><span data-stu-id="023dc-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="023dc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="023dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="023dc-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="023dc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="023dc-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="023dc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="023dc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="023dc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="023dc-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="023dc-110">Called by:</span></span>  <br/> |<span data-ttu-id="023dc-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="023dc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="023dc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="023dc-112">Parameters</span></span>

 <span data-ttu-id="023dc-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="023dc-113">_Minuend_</span></span>
  
> <span data-ttu-id="023dc-114">no Uma estrutura [FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado a partir do qual o valor no parâmetro _subtrahend_ deve ser subtraído.</span><span class="sxs-lookup"><span data-stu-id="023dc-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="023dc-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="023dc-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="023dc-116">no Uma estrutura **FILETIME** que contém o inteiro de 64 bits não assinado que é subtraído do valor indicado pelo parâmetro _minuend_ .</span><span class="sxs-lookup"><span data-stu-id="023dc-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="023dc-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="023dc-117">Return value</span></span>

<span data-ttu-id="023dc-118">A função **FtSubFt** retorna uma estrutura **FILETIME** que contém o resultado da subtração.</span><span class="sxs-lookup"><span data-stu-id="023dc-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="023dc-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="023dc-119">The two input parameters remain unchanged.</span></span> 
  

