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
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766540"
---
# <a name="fequalnames"></a><span data-ttu-id="89c41-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="89c41-103">FEqualNames</span></span>

  
  
<span data-ttu-id="89c41-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89c41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89c41-105">Determina se o MAPI duas propriedades nomeadas são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="89c41-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89c41-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="89c41-106">Header file:</span></span>  <br/> |<span data-ttu-id="89c41-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="89c41-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="89c41-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="89c41-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="89c41-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="89c41-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="89c41-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="89c41-110">Called by:</span></span>  <br/> |<span data-ttu-id="89c41-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="89c41-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="89c41-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89c41-112">Parameters</span></span>

 <span data-ttu-id="89c41-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="89c41-113">_lpName1_</span></span>
  
> <span data-ttu-id="89c41-114">[in] Ponteiro para uma estrutura [MAPINAMEID](mapinameid.md) descrevendo a primeira propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="89c41-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="89c41-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="89c41-115">_lpName2_</span></span>
  
> <span data-ttu-id="89c41-116">[in] Ponteiro para uma estrutura **MAPINAMEID** descrevendo a segunda propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="89c41-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89c41-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="89c41-117">Return value</span></span>

<span data-ttu-id="89c41-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="89c41-118">TRUE</span></span> 
  
> <span data-ttu-id="89c41-119">Os nomes das duas propriedades são iguais.</span><span class="sxs-lookup"><span data-stu-id="89c41-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="89c41-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="89c41-120">FALSE</span></span> 
  
> <span data-ttu-id="89c41-121">Os nomes das duas propriedades não são iguais.</span><span class="sxs-lookup"><span data-stu-id="89c41-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89c41-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="89c41-122">Remarks</span></span>

<span data-ttu-id="89c41-123">A função **FEqualNames** é útil porque a estrutura **MAPINAMEID** contém um [GUID](guid.md) e pode representar o próprio nome de propriedade em mais de uma forma.</span><span class="sxs-lookup"><span data-stu-id="89c41-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="89c41-124">Isso significa que as duas estruturas não podem ser comparadas pelos métodos binários simples.</span><span class="sxs-lookup"><span data-stu-id="89c41-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="89c41-125">O processo de teste diferencia maiusculas de minúsculas para as cadeias de caracteres de nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="89c41-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

