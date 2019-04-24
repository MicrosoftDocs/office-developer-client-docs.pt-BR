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
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357481"
---
# <a name="sccopynotifications"></a><span data-ttu-id="996fa-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="996fa-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="996fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="996fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="996fa-105">Copia um grupo de notificações de eventos para um único bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="996fa-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="996fa-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="996fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="996fa-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="996fa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="996fa-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="996fa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="996fa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="996fa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="996fa-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="996fa-110">Called by:</span></span>  <br/> |<span data-ttu-id="996fa-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="996fa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="996fa-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="996fa-112">Parameters</span></span>

 <span data-ttu-id="996fa-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="996fa-113">_cntf_</span></span>
  
> <span data-ttu-id="996fa-114">no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="996fa-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="996fa-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="996fa-115">_rgntf_</span></span>
  
> <span data-ttu-id="996fa-116">no Ponteiro para uma matriz de estruturas de **notificação** que define as notificações de eventos a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="996fa-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="996fa-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="996fa-117">_pvDst_</span></span>
  
> <span data-ttu-id="996fa-118">bota Ponteiro para as notificações retornadas.</span><span class="sxs-lookup"><span data-stu-id="996fa-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="996fa-119">_PCB_</span><span class="sxs-lookup"><span data-stu-id="996fa-119">_pcb_</span></span>
  
> <span data-ttu-id="996fa-120">bota Ponteiro opcional para uma variável onde o tamanho, em bytes, da matriz apontada pelo parâmetro _rgntf_ é armazenado.</span><span class="sxs-lookup"><span data-stu-id="996fa-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="996fa-121">Se não for nulo, o parâmetro _PCB_ será definido como o número de bytes armazenados no parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="996fa-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="996fa-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="996fa-122">Return value</span></span>

<span data-ttu-id="996fa-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="996fa-123">S_OK</span></span>
  
> <span data-ttu-id="996fa-124">As notificações de eventos foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="996fa-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="996fa-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="996fa-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="996fa-126">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="996fa-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="996fa-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="996fa-127">Remarks</span></span>

<span data-ttu-id="996fa-128">Se NULL for passado no parâmetro _PCB_ , nenhuma cópia será executada; se um valor não nulo é passado no _PCB_, a função **ScCopyNotifications** copia o tamanho da matriz e a própria matriz para um único bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="996fa-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="996fa-129">Se _PCB_ não for nulo, será definido como o número de bytes armazenados no parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="996fa-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="996fa-130">O parâmetro _pvDst_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="996fa-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

