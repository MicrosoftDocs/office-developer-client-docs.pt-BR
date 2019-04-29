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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417200"
---
# <a name="mscapselector"></a><span data-ttu-id="bfdaf-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="bfdaf-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="bfdaf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfdaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfdaf-105">Especifica as funcionalidades a serem retornadas para um repositório.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bfdaf-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bfdaf-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="bfdaf-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bfdaf-107">Members</span></span>

 <span data-ttu-id="bfdaf-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="bfdaf-109">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="bfdaf-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="bfdaf-111">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="bfdaf-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="bfdaf-113">Recursos sobre as pastas de suporte em um repositório.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="bfdaf-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="bfdaf-115">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="bfdaf-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="bfdaf-117">Recursos sobre restrições de suporte em um repositório.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-117">Capabilities about supporting restrictions on a store.</span></span>
    

