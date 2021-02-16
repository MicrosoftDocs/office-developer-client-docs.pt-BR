---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Uma variável desse tipo de dados contém o valor de uma propriedade, que é de um tipo de dados variante.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424396"
---
# <a name="acct_variant"></a><span data-ttu-id="7e67e-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="7e67e-103">ACCT_VARIANT</span></span>

<span data-ttu-id="7e67e-104">Uma variável desse tipo de dados contém o valor de uma propriedade, que é de um tipo de dados variante.</span><span class="sxs-lookup"><span data-stu-id="7e67e-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e67e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7e67e-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7e67e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7e67e-106">Members</span></span>

<span data-ttu-id="7e67e-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="7e67e-107">_dwType_</span></span>
  
> <span data-ttu-id="7e67e-108">Tipo de variante:</span><span class="sxs-lookup"><span data-stu-id="7e67e-108">Type of variant:</span></span>
    
    - <span data-ttu-id="7e67e-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7e67e-109">PT_LONG</span></span>
    
    - <span data-ttu-id="7e67e-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e67e-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="7e67e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7e67e-111">PT_BINARY</span></span>
    
<span data-ttu-id="7e67e-112">_dw_</span><span class="sxs-lookup"><span data-stu-id="7e67e-112">_dw_</span></span>
  
> <span data-ttu-id="7e67e-113">Valor DWORD da variante.</span><span class="sxs-lookup"><span data-stu-id="7e67e-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="7e67e-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="7e67e-114">_pwsz_</span></span>
  
> <span data-ttu-id="7e67e-115">Valor da cadeia de caracteres da variante.</span><span class="sxs-lookup"><span data-stu-id="7e67e-115">String value of variant.</span></span>
    
<span data-ttu-id="7e67e-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="7e67e-116">_bin_</span></span>
  
> <span data-ttu-id="7e67e-117">Valor binário da variante.</span><span class="sxs-lookup"><span data-stu-id="7e67e-117">Binary value of the variant.</span></span>
    

