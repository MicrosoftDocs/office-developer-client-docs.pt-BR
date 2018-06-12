---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Uma variável desse tipo de dados contém o valor de uma propriedade, que é um tipo de dados variant.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765795"
---
# <a name="acctvariant"></a><span data-ttu-id="6c436-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="6c436-103">ACCT_VARIANT</span></span>

<span data-ttu-id="6c436-104">Uma variável desse tipo de dados contém o valor de uma propriedade, que é um tipo de dados variant.</span><span class="sxs-lookup"><span data-stu-id="6c436-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6c436-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6c436-105">Quick info</span></span>

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a><span data-ttu-id="6c436-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6c436-106">Members</span></span>

<span data-ttu-id="6c436-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="6c436-107">_dwType_</span></span>
  
> <span data-ttu-id="6c436-108">Tipo de variante:</span><span class="sxs-lookup"><span data-stu-id="6c436-108">Type of variant:</span></span>
    
    - <span data-ttu-id="6c436-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c436-109">PT_LONG</span></span>
    
    - <span data-ttu-id="6c436-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c436-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="6c436-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6c436-111">PT_BINARY</span></span>
    
<span data-ttu-id="6c436-112">_data warehouse_</span><span class="sxs-lookup"><span data-stu-id="6c436-112">_dw_</span></span>
  
> <span data-ttu-id="6c436-113">Valor DWORD da variante.</span><span class="sxs-lookup"><span data-stu-id="6c436-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="6c436-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="6c436-114">_pwsz_</span></span>
  
> <span data-ttu-id="6c436-115">O valor da variante de sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c436-115">String value of variant.</span></span>
    
<span data-ttu-id="6c436-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="6c436-116">_bin_</span></span>
  
> <span data-ttu-id="6c436-117">Valor binário da variante.</span><span class="sxs-lookup"><span data-stu-id="6c436-117">Binary value of the variant.</span></span>
    

