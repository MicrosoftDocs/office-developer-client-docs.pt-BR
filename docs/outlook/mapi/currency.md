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
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315131"
---
# <a name="currency"></a><span data-ttu-id="fc6c2-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="fc6c2-103">CURRENCY</span></span>

  
  
<span data-ttu-id="fc6c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc6c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc6c2-105">Contém um inteiro de 64 bits assinado que representa um valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc6c2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fc6c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc6c2-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fc6c2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="fc6c2-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc6c2-108">Members</span></span>

 <span data-ttu-id="fc6c2-109">**Baixo**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-109">**Lo**</span></span>
  
> <span data-ttu-id="fc6c2-110">Bits de 32 de ordem inferior do valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="fc6c2-111">**Oi**</span><span class="sxs-lookup"><span data-stu-id="fc6c2-111">**Hi**</span></span>
  
> <span data-ttu-id="fc6c2-112">Alta ordem 32 bits do valor da moeda.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc6c2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc6c2-113">Remarks</span></span>

<span data-ttu-id="fc6c2-114">A estrutura de **moeda** é uma representação inteira em escala de um número decimal com quatro dígitos à direita da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="fc6c2-115">Por exemplo, um valor armazenado de 327500 deve ser interpretado como representando um valor de moeda de 32,7500.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="fc6c2-116">A estrutura de **moeda** é usada para descrever uma propriedade do tipo PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="fc6c2-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="fc6c2-117">Para obter informações sobre tipos de propriedade, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc6c2-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc6c2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc6c2-118">See also</span></span>



[<span data-ttu-id="fc6c2-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fc6c2-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="fc6c2-120">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc6c2-120">MAPI Structures</span></span>](mapi-structures.md)

