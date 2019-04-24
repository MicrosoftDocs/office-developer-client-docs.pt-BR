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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334878"
---
# <a name="fequalnames"></a><span data-ttu-id="240c2-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="240c2-103">FEqualNames</span></span>

  
  
<span data-ttu-id="240c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="240c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="240c2-105">Determina se duas propriedades nomeadas por MAPI são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="240c2-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="240c2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="240c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="240c2-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="240c2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="240c2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="240c2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="240c2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="240c2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="240c2-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="240c2-110">Called by:</span></span>  <br/> |<span data-ttu-id="240c2-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="240c2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="240c2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="240c2-112">Parameters</span></span>

 <span data-ttu-id="240c2-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="240c2-113">_lpName1_</span></span>
  
> <span data-ttu-id="240c2-114">no Ponteiro para uma estrutura [MAPINAMEID](mapinameid.md) descrevendo a primeira propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="240c2-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="240c2-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="240c2-115">_lpName2_</span></span>
  
> <span data-ttu-id="240c2-116">no Ponteiro para uma estrutura **MAPINAMEID** descrevendo a segunda propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="240c2-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="240c2-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="240c2-117">Return value</span></span>

<span data-ttu-id="240c2-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="240c2-118">TRUE</span></span> 
  
> <span data-ttu-id="240c2-119">Os dois nomes de propriedade são iguais.</span><span class="sxs-lookup"><span data-stu-id="240c2-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="240c2-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="240c2-120">FALSE</span></span> 
  
> <span data-ttu-id="240c2-121">Os dois nomes de propriedade não são iguais.</span><span class="sxs-lookup"><span data-stu-id="240c2-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="240c2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="240c2-122">Remarks</span></span>

<span data-ttu-id="240c2-123">A função **FEqualNames** é útil porque a estrutura **MAPINAMEID** contém um [GUID](guid.md) e pode representar o próprio nome da propriedade em mais de uma forma.</span><span class="sxs-lookup"><span data-stu-id="240c2-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="240c2-124">Isso significa que as duas estruturas não podem ser comparadas por métodos binários simples.</span><span class="sxs-lookup"><span data-stu-id="240c2-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="240c2-125">O processo de teste diferencia maiúsculas de minúsculas para as cadeias de caracteres de nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="240c2-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

