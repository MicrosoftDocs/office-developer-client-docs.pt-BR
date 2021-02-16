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
# <a name="mscap_selector"></a><span data-ttu-id="aff86-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="aff86-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="aff86-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aff86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aff86-105">Especifica os recursos a retornar para um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aff86-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aff86-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aff86-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="aff86-107">Membros</span><span class="sxs-lookup"><span data-stu-id="aff86-107">Members</span></span>

 <span data-ttu-id="aff86-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="aff86-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="aff86-109">Este membro está reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="aff86-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="aff86-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="aff86-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="aff86-111">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="aff86-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="aff86-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="aff86-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="aff86-113">Recursos sobre suporte a pastas em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aff86-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="aff86-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="aff86-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="aff86-115">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="aff86-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="aff86-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="aff86-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="aff86-117">Recursos sobre o suporte a restrições em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aff86-117">Capabilities about supporting restrictions on a store.</span></span>
    

