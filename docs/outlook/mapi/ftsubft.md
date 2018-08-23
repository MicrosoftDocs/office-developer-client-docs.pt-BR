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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578259"
---
# <a name="ftsubft"></a><span data-ttu-id="0dbd5-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="0dbd5-103">FtSubFt</span></span>

  
  
<span data-ttu-id="0dbd5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dbd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dbd5-105">Subtrai um inteiro não assinado de 64 bits do outro.</span><span class="sxs-lookup"><span data-stu-id="0dbd5-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dbd5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0dbd5-106">Header file:</span></span>  <br/> |<span data-ttu-id="0dbd5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0dbd5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0dbd5-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0dbd5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0dbd5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0dbd5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0dbd5-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0dbd5-110">Called by:</span></span>  <br/> |<span data-ttu-id="0dbd5-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0dbd5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="0dbd5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dbd5-112">Parameters</span></span>

 <span data-ttu-id="0dbd5-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="0dbd5-113">_Minuend_</span></span>
  
> <span data-ttu-id="0dbd5-114">[in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits do qual o valor no parâmetro _Subtrahend_ deve ser subtraídos.</span><span class="sxs-lookup"><span data-stu-id="0dbd5-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="0dbd5-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="0dbd5-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="0dbd5-116">[in] Uma estrutura **FILETIME** que contém o inteiro não assinado de 64 bits é subtraído do valor indicado pelo parâmetro _Minuend_ .</span><span class="sxs-lookup"><span data-stu-id="0dbd5-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0dbd5-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0dbd5-117">Return value</span></span>

<span data-ttu-id="0dbd5-118">A função **FtSubFt** retorna uma estrutura **FILETIME** que contém o resultado de subtração.</span><span class="sxs-lookup"><span data-stu-id="0dbd5-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="0dbd5-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="0dbd5-119">The two input parameters remain unchanged.</span></span> 
  

