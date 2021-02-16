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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418719"
---
# <a name="getinstance"></a><span data-ttu-id="9f218-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="9f218-103">GetInstance</span></span>

  
  
<span data-ttu-id="9f218-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f218-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f218-105">Copia um valor dentro de uma propriedade de múltiplos valores para uma propriedade de valor único do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="9f218-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f218-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9f218-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f218-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="9f218-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="9f218-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9f218-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f218-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f218-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f218-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9f218-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f218-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9f218-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="9f218-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f218-112">Parameters</span></span>

 <span data-ttu-id="9f218-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="9f218-113">_pvalMv_</span></span>
  
> <span data-ttu-id="9f218-114">[in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo uma propriedade de múltiplos valores.</span><span class="sxs-lookup"><span data-stu-id="9f218-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="9f218-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="9f218-115">_pvalSv_</span></span>
  
> <span data-ttu-id="9f218-116">[in] Ponteiro para uma propriedade de valor único para receber dados.</span><span class="sxs-lookup"><span data-stu-id="9f218-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="9f218-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="9f218-117">_uliInst_</span></span>
  
> <span data-ttu-id="9f218-118">[in] O número da instância, ou seja, o elemento da matriz, do valor que está sendo copiado da estrutura indicada pelo _parâmetro pvalMv._</span><span class="sxs-lookup"><span data-stu-id="9f218-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f218-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9f218-119">Return value</span></span>

<span data-ttu-id="9f218-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9f218-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f218-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f218-121">Remarks</span></span>

<span data-ttu-id="9f218-122">Se o valor copiado for muito grande para a memória alocada, a função **GetInstance** só copiará ponteiros em vez de alocar nova memória.</span><span class="sxs-lookup"><span data-stu-id="9f218-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

