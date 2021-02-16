---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414799"
---
# <a name="fequalnames"></a><span data-ttu-id="7eedb-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="7eedb-103">FEqualNames</span></span>

  
  
<span data-ttu-id="7eedb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eedb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eedb-105">Determina se duas propriedades nomeadas MAPI são iguais.</span><span class="sxs-lookup"><span data-stu-id="7eedb-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7eedb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7eedb-106">Header file:</span></span>  <br/> |<span data-ttu-id="7eedb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7eedb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7eedb-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7eedb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7eedb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7eedb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7eedb-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="7eedb-110">Called by:</span></span>  <br/> |<span data-ttu-id="7eedb-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="7eedb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="7eedb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eedb-112">Parameters</span></span>

 <span data-ttu-id="7eedb-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="7eedb-113">_lpName1_</span></span>
  
> <span data-ttu-id="7eedb-114">[in] Ponteiro para uma [estrutura MAPINAMEID que](mapinameid.md) descreve a primeira propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="7eedb-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="7eedb-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="7eedb-115">_lpName2_</span></span>
  
> <span data-ttu-id="7eedb-116">[in] Ponteiro para uma **estrutura MAPINAMEID que** descreve a segunda propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="7eedb-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7eedb-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7eedb-117">Return value</span></span>

<span data-ttu-id="7eedb-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="7eedb-118">TRUE</span></span> 
  
> <span data-ttu-id="7eedb-119">Os dois nomes de propriedade são iguais.</span><span class="sxs-lookup"><span data-stu-id="7eedb-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="7eedb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="7eedb-120">FALSE</span></span> 
  
> <span data-ttu-id="7eedb-121">Os dois nomes de propriedade não são iguais.</span><span class="sxs-lookup"><span data-stu-id="7eedb-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7eedb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eedb-122">Remarks</span></span>

<span data-ttu-id="7eedb-123">A **função FEqualNames** é útil porque a estrutura **MAPINAMEID** contém um [GUID](guid.md) e pode representar o nome da propriedade em si de mais de uma maneira.</span><span class="sxs-lookup"><span data-stu-id="7eedb-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="7eedb-124">Isso significa que as duas estruturas não podem ser comparadas por métodos binários simples.</span><span class="sxs-lookup"><span data-stu-id="7eedb-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="7eedb-125">O processo de teste faz a seleção de caso para as cadeias de caracteres do nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7eedb-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

