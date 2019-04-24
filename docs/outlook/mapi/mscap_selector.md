---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338672"
---
# <a name="mscapselector"></a><span data-ttu-id="48070-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="48070-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="48070-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48070-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48070-105">Especifica as funcionalidades a serem retornadas para um repositório.</span><span class="sxs-lookup"><span data-stu-id="48070-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="48070-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="48070-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="48070-107">Membros</span><span class="sxs-lookup"><span data-stu-id="48070-107">Members</span></span>

 <span data-ttu-id="48070-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="48070-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="48070-109">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="48070-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="48070-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="48070-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="48070-111">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="48070-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="48070-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="48070-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="48070-113">Recursos sobre as pastas de suporte em um repositório.</span><span class="sxs-lookup"><span data-stu-id="48070-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="48070-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="48070-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="48070-115">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="48070-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="48070-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="48070-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="48070-117">Recursos sobre restrições de suporte em um repositório.</span><span class="sxs-lookup"><span data-stu-id="48070-117">Capabilities about supporting restrictions on a store.</span></span>
    

