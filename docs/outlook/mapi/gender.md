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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428645"
---
# <a name="gender"></a><span data-ttu-id="123b2-103">Gênero</span><span class="sxs-lookup"><span data-stu-id="123b2-103">Gender</span></span>

  
  
<span data-ttu-id="123b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="123b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="123b2-105">Especifica os valores possíveis para o sexo de um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="123b2-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="123b2-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="123b2-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="123b2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="123b2-107">Members</span></span>

 <span data-ttu-id="123b2-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="123b2-108">_genderMin_</span></span>
  
> <span data-ttu-id="123b2-109">O número mínimo de valores diferentes suportados para o sexo.</span><span class="sxs-lookup"><span data-stu-id="123b2-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="123b2-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="123b2-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="123b2-111">O sexo não é especificado para o usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="123b2-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="123b2-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="123b2-112">_genderFemale_</span></span>
  
> <span data-ttu-id="123b2-113">O usuário de mensagens é fêmea.</span><span class="sxs-lookup"><span data-stu-id="123b2-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="123b2-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="123b2-114">_genderMale_</span></span>
  
> <span data-ttu-id="123b2-115">O usuário de mensagens é macho.</span><span class="sxs-lookup"><span data-stu-id="123b2-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="123b2-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="123b2-116">_genderCount_</span></span>
  
> <span data-ttu-id="123b2-117">O número de valores diferentes suportados para o sexo.</span><span class="sxs-lookup"><span data-stu-id="123b2-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="123b2-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="123b2-118">_genderMax_</span></span>
  
> <span data-ttu-id="123b2-119">O número máximo de valores diferentes com suporte para o sexo.</span><span class="sxs-lookup"><span data-stu-id="123b2-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="123b2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="123b2-120">See also</span></span>



[<span data-ttu-id="123b2-121">Propriedade canônica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="123b2-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

