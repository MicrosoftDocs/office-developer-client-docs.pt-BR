---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766628"
---
# <a name="ftmuldw"></a><span data-ttu-id="70be2-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="70be2-103">FtMulDw</span></span>

  
  
<span data-ttu-id="70be2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70be2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70be2-105">Multiplica um inteiro de 64 bits não assinado por um inteiro não assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="70be2-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70be2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="70be2-106">Header file:</span></span>  <br/> |<span data-ttu-id="70be2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="70be2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="70be2-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="70be2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="70be2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="70be2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="70be2-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="70be2-110">Called by:</span></span>  <br/> |<span data-ttu-id="70be2-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="70be2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="70be2-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="70be2-112">Parameters</span></span>

 <span data-ttu-id="70be2-113">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="70be2-113">_Multiplier_</span></span>
  
> <span data-ttu-id="70be2-114">[in] Uma palavra dupla que contém o multiplicador de inteiro não assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="70be2-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="70be2-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="70be2-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="70be2-116">[in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits seja multiplicado pelo valor no parâmetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="70be2-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="70be2-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="70be2-117">Return value</span></span>

<span data-ttu-id="70be2-118">A função **FtMulDw** retorna uma estrutura **FILETIME** que contém o produto dos dois valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="70be2-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="70be2-119">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="70be2-119">The two input parameters remain unchanged.</span></span> 
  

