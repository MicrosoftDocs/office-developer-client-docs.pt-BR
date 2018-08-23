---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593351"
---
# <a name="sccopynotifications"></a><span data-ttu-id="f4ad0-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="f4ad0-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="f4ad0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4ad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4ad0-105">Copia um grupo de notificações de evento para um único bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4ad0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f4ad0-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4ad0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f4ad0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f4ad0-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f4ad0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4ad0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4ad0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4ad0-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f4ad0-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4ad0-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f4ad0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f4ad0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4ad0-112">Parameters</span></span>

 <span data-ttu-id="f4ad0-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="f4ad0-113">_cntf_</span></span>
  
> <span data-ttu-id="f4ad0-114">[in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="f4ad0-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f4ad0-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="f4ad0-115">_rgntf_</span></span>
  
> <span data-ttu-id="f4ad0-116">[in] Ponteiro para uma matriz de estruturas de **notificação** , definindo as notificações de evento a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="f4ad0-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="f4ad0-117">_pvDst_</span></span>
  
> <span data-ttu-id="f4ad0-118">[out] Ponteiro para as notificações retornados.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="f4ad0-119">_PCB_</span><span class="sxs-lookup"><span data-stu-id="f4ad0-119">_pcb_</span></span>
  
> <span data-ttu-id="f4ad0-120">[out] Opcional ponteiro para uma variável onde o tamanho, em bytes, da matriz apontado pelo parâmetro _rgntf_ é armazenado.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="f4ad0-121">Se não for NULL, o parâmetro _pcb_ estiver definido como o número de bytes armazenado no parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="f4ad0-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4ad0-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f4ad0-122">Return value</span></span>

<span data-ttu-id="f4ad0-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4ad0-123">S_OK</span></span>
  
> <span data-ttu-id="f4ad0-124">Notificações de evento foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="f4ad0-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f4ad0-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="f4ad0-126">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4ad0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4ad0-127">Remarks</span></span>

<span data-ttu-id="f4ad0-128">Se NULL é passada no parâmetro _pcb_ , cópia não é executada; Se um valor não-nulo é passado _pcb_, a função **ScCopyNotifications** copia o tamanho da matriz e do próprio conjunto para um único bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="f4ad0-129">Se _pcb_ não for nula, ela é definida como o número de bytes armazenado no parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="f4ad0-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="f4ad0-130">O parâmetro _pvDst_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="f4ad0-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

