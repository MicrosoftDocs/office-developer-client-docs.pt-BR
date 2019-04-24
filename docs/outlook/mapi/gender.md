---
title: Gênero
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342578"
---
# <a name="gender"></a><span data-ttu-id="182df-103">Gênero</span><span class="sxs-lookup"><span data-stu-id="182df-103">Gender</span></span>

  
  
<span data-ttu-id="182df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="182df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="182df-105">Especifica os valores possíveis para o sexo de um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="182df-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="182df-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="182df-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="182df-107">Membros</span><span class="sxs-lookup"><span data-stu-id="182df-107">Members</span></span>

 <span data-ttu-id="182df-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="182df-108">_genderMin_</span></span>
  
> <span data-ttu-id="182df-109">O número mínimo de valores diferentes suportados para o sexo.</span><span class="sxs-lookup"><span data-stu-id="182df-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="182df-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="182df-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="182df-111">O sexo não é especificado para o usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="182df-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="182df-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="182df-112">_genderFemale_</span></span>
  
> <span data-ttu-id="182df-113">O usuário de mensagens é fêmea.</span><span class="sxs-lookup"><span data-stu-id="182df-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="182df-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="182df-114">_genderMale_</span></span>
  
> <span data-ttu-id="182df-115">O usuário de mensagens é macho.</span><span class="sxs-lookup"><span data-stu-id="182df-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="182df-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="182df-116">_genderCount_</span></span>
  
> <span data-ttu-id="182df-117">O número de valores diferentes suportados para o sexo.</span><span class="sxs-lookup"><span data-stu-id="182df-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="182df-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="182df-118">_genderMax_</span></span>
  
> <span data-ttu-id="182df-119">O número máximo de valores diferentes com suporte para o sexo.</span><span class="sxs-lookup"><span data-stu-id="182df-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="182df-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="182df-120">See also</span></span>



[<span data-ttu-id="182df-121">Propriedade canônica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="182df-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

