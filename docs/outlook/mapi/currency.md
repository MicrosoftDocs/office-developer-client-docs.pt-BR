---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766368"
---
# <a name="currency"></a><span data-ttu-id="ea696-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ea696-103">CURRENCY</span></span>

  
  
<span data-ttu-id="ea696-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea696-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea696-105">Contém um inteiro assinado de 64 bits representando um valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="ea696-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea696-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ea696-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea696-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea696-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="ea696-108">Members</span><span class="sxs-lookup"><span data-stu-id="ea696-108">Members</span></span>

 <span data-ttu-id="ea696-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="ea696-109">**Lo**</span></span>
  
> <span data-ttu-id="ea696-110">Ordem baixa de 32 bits do valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="ea696-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="ea696-111">**Oi**</span><span class="sxs-lookup"><span data-stu-id="ea696-111">**Hi**</span></span>
  
> <span data-ttu-id="ea696-112">Ordem alta de 32 bits do valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="ea696-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea696-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea696-113">Remarks</span></span>

<span data-ttu-id="ea696-114">A estrutura de **moeda** é uma representação de inteiro em escala de um número decimal com quatro dígitos à direita da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="ea696-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="ea696-115">Por exemplo, um valor armazenado de 327500 deve ser interpretado como representando um valor de moeda da 32.7500.</span><span class="sxs-lookup"><span data-stu-id="ea696-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="ea696-116">A estrutura de **moeda** é usada para descrever uma propriedade do tipo PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="ea696-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="ea696-117">Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea696-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea696-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea696-118">See also</span></span>



[<span data-ttu-id="ea696-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ea696-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ea696-120">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ea696-120">MAPI Structures</span></span>](mapi-structures.md)

