---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588122"
---
# <a name="mscapselector"></a><span data-ttu-id="07cdc-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="07cdc-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="07cdc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07cdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07cdc-105">Especifica os recursos para retornar para um repositório.</span><span class="sxs-lookup"><span data-stu-id="07cdc-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="07cdc-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="07cdc-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="07cdc-107">Members</span><span class="sxs-lookup"><span data-stu-id="07cdc-107">Members</span></span>

 <span data-ttu-id="07cdc-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="07cdc-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="07cdc-109">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="07cdc-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="07cdc-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="07cdc-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="07cdc-111">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="07cdc-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="07cdc-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="07cdc-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="07cdc-113">Recursos sobre o suporte a pastas em um repositório.</span><span class="sxs-lookup"><span data-stu-id="07cdc-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="07cdc-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="07cdc-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="07cdc-115">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="07cdc-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="07cdc-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="07cdc-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="07cdc-117">Recursos sobre o suporte a restrições em um repositório.</span><span class="sxs-lookup"><span data-stu-id="07cdc-117">Capabilities about supporting restrictions on a store.</span></span>
    

