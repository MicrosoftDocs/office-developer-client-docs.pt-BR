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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588451"
---
# <a name="gender"></a><span data-ttu-id="05db9-103">Gênero</span><span class="sxs-lookup"><span data-stu-id="05db9-103">Gender</span></span>

  
  
<span data-ttu-id="05db9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05db9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05db9-105">Especifica os valores possíveis para o gênero de um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="05db9-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="05db9-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="05db9-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="05db9-107">Members</span><span class="sxs-lookup"><span data-stu-id="05db9-107">Members</span></span>

 <span data-ttu-id="05db9-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="05db9-108">_genderMin_</span></span>
  
> <span data-ttu-id="05db9-109">O número mínimo de diferentes valores suportados para o gênero.</span><span class="sxs-lookup"><span data-stu-id="05db9-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="05db9-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="05db9-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="05db9-111">O gênero não for especificado para o usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="05db9-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="05db9-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="05db9-112">_genderFemale_</span></span>
  
> <span data-ttu-id="05db9-113">O usuário de mensagens é feminino.</span><span class="sxs-lookup"><span data-stu-id="05db9-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="05db9-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="05db9-114">_genderMale_</span></span>
  
> <span data-ttu-id="05db9-115">O usuário de mensagens é Masculino.</span><span class="sxs-lookup"><span data-stu-id="05db9-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="05db9-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="05db9-116">_genderCount_</span></span>
  
> <span data-ttu-id="05db9-117">O número de diferentes valores suportados para o gênero.</span><span class="sxs-lookup"><span data-stu-id="05db9-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="05db9-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="05db9-118">_genderMax_</span></span>
  
> <span data-ttu-id="05db9-119">O número máximo de diferentes valores suportados para o gênero.</span><span class="sxs-lookup"><span data-stu-id="05db9-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05db9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="05db9-120">See also</span></span>



[<span data-ttu-id="05db9-121">Propriedade canônico de PidTagGender</span><span class="sxs-lookup"><span data-stu-id="05db9-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

