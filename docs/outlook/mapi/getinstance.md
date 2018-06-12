---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766665"
---
# <a name="getinstance"></a><span data-ttu-id="d74c1-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="d74c1-103">GetInstance</span></span>

  
  
<span data-ttu-id="d74c1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d74c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d74c1-105">Copia um valor dentro de uma propriedade de vários valores para uma propriedade de valor único do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="d74c1-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d74c1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d74c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="d74c1-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="d74c1-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="d74c1-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d74c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d74c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d74c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d74c1-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d74c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="d74c1-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="d74c1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="d74c1-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d74c1-112">Parameters</span></span>

 <span data-ttu-id="d74c1-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="d74c1-113">_pvalMv_</span></span>
  
> <span data-ttu-id="d74c1-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo uma propriedade de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="d74c1-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="d74c1-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="d74c1-115">_pvalSv_</span></span>
  
> <span data-ttu-id="d74c1-116">[in] Ponteiro para uma propriedade de valor único para receber dados.</span><span class="sxs-lookup"><span data-stu-id="d74c1-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="d74c1-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="d74c1-117">_uliInst_</span></span>
  
> <span data-ttu-id="d74c1-118">[in] O número de instância, ou seja, o elemento de matriz, do valor que está sendo copiado da estrutura de indicado pelo parâmetro _pvalMv_ .</span><span class="sxs-lookup"><span data-stu-id="d74c1-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d74c1-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d74c1-119">Return value</span></span>

<span data-ttu-id="d74c1-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d74c1-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d74c1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d74c1-121">Remarks</span></span>

<span data-ttu-id="d74c1-122">Se o valor copiado for muito grande para a memória alocada, a função **GetInstance** copia somente ponteiros em vez de alocar nova memória.</span><span class="sxs-lookup"><span data-stu-id="d74c1-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

