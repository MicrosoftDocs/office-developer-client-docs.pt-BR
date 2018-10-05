---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401276"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="b7499-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7499-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="b7499-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7499-105">Fornece informações para um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="b7499-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7499-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="b7499-106">Provided by:</span></span>  <br/> |<span data-ttu-id="b7499-107">Consulta em [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="b7499-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="b7499-108">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b7499-108">Called by:</span></span>  <br/> |<span data-ttu-id="b7499-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="b7499-109">Client</span></span>  <br/> |
|<span data-ttu-id="b7499-110">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b7499-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b7499-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b7499-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b7499-112">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="b7499-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7499-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="b7499-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="b7499-114">Define o estado atual de um objeto offline para online ou offline.</span><span class="sxs-lookup"><span data-stu-id="b7499-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="b7499-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="b7499-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="b7499-116">Obtém as condições para o qual os retornos de chamada são suportados por um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="b7499-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="b7499-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="b7499-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="b7499-118">Obtém o estado atual de online ou offline, de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="b7499-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="b7499-119">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="b7499-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="b7499-120">Este membro é um espaço reservado e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="b7499-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7499-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7499-121">Remarks</span></span>

<span data-ttu-id="b7499-122">Um cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** abrir e obter um objeto offline que ofereça suporte a **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="b7499-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="b7499-123">Como **IMAPIOfflineMgr** herda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), o cliente pode consultar a esta interface (usando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obter um ponteiro para o ponteiro de interface **IMAPIOffline** para o objeto offline.</span><span class="sxs-lookup"><span data-stu-id="b7499-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="b7499-124">O cliente pode então obter ou definir o estado atual do objeto, ou Saiba mais sobre os recursos de retorno de chamada do objeto (chamando **IMAPIOffline::GetCapabilities** ) e optar por configurar retornos de chamada usando **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="b7499-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="b7499-125">Um membro nesta interface é um espaço reservado reservado para uso interno do Microsoft Outlook 2013 e está sujeita a alterações.</span><span class="sxs-lookup"><span data-stu-id="b7499-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="b7499-126">Outros membros nessa interface devem ser usados apenas como documentado.</span><span class="sxs-lookup"><span data-stu-id="b7499-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7499-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7499-127">See also</span></span>



[<span data-ttu-id="b7499-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="b7499-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="b7499-129">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="b7499-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="b7499-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b7499-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b7499-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b7499-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

