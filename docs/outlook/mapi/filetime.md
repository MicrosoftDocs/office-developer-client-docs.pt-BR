---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583250"
---
# <a name="filetime"></a><span data-ttu-id="eb209-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="eb209-103">FILETIME</span></span>

  
  
<span data-ttu-id="eb209-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb209-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb209-105">Contém uma data de 64 bits não assinada e o valor de tempo para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb209-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="eb209-106">Esse valor representa o número de unidades de 100 nanossegundos, desde o início do dia 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="eb209-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb209-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eb209-107">Header file:</span></span>  <br/> |<span data-ttu-id="eb209-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb209-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="eb209-109">Members</span><span class="sxs-lookup"><span data-stu-id="eb209-109">Members</span></span>

 <span data-ttu-id="eb209-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="eb209-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="eb209-111">Valor de tempo de 32 bits de ordem baixa do arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb209-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="eb209-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="eb209-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="eb209-113">Valor de tempo de 32 bits de ordem alta do arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb209-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb209-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb209-114">Remarks</span></span>

<span data-ttu-id="eb209-115">Uma propriedade do tipo PT_SYSTIME tem uma estrutura **FILETIME** para seu valor.</span><span class="sxs-lookup"><span data-stu-id="eb209-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="eb209-116">Essa propriedade tem um tipo de dados **FILETIME** para o membro de **valor** em sua definição em uma estrutura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="eb209-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="eb209-117">A definição da estrutura **FILETIME** está na _referência do programador do Win32_ e no arquivo de cabeçalho de MAPI Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="eb209-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="eb209-118">MAPI define a estrutura condicionalmente para certificar-se de que ela é definida quando a definição de Win32 não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="eb209-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb209-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb209-119">See also</span></span>



[<span data-ttu-id="eb209-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eb209-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="eb209-121">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="eb209-121">MAPI Structures</span></span>](mapi-structures.md)

