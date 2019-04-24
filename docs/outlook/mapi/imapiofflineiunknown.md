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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321263"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="acf7b-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="acf7b-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="acf7b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acf7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acf7b-105">Fornece informações sobre um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="acf7b-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="acf7b-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="acf7b-106">Provided by:</span></span>  <br/> |<span data-ttu-id="acf7b-107">Consulta no [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="acf7b-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="acf7b-108">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="acf7b-108">Called by:</span></span>  <br/> |<span data-ttu-id="acf7b-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="acf7b-109">Client</span></span>  <br/> |
|<span data-ttu-id="acf7b-110">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="acf7b-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="acf7b-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="acf7b-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="acf7b-112">Vtable order</span><span class="sxs-lookup"><span data-stu-id="acf7b-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acf7b-113">**[SetCurrentstate](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="acf7b-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="acf7b-114">Define o estado atual de um objeto offline para online ou offline.</span><span class="sxs-lookup"><span data-stu-id="acf7b-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="acf7b-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="acf7b-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="acf7b-116">Obtém as condições para as quais os retornos de chamada são compatíveis com um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="acf7b-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="acf7b-117">**[GetCurrentstate](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="acf7b-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="acf7b-118">Obtém o estado online ou offline atual de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="acf7b-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="acf7b-119">*Membro PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="acf7b-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="acf7b-120">Esse membro é um espaço reservado e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="acf7b-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acf7b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="acf7b-121">Remarks</span></span>

<span data-ttu-id="acf7b-122">Um cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** para abrir e obter um objeto offline que oferece suporte a **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="acf7b-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="acf7b-123">Como o **IMAPIOfflineMgr** herda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), o cliente pode consultar esta interface (usando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obter um ponteiro para o ponteiro de interface do **IMAPIOffline** para o objeto offline.</span><span class="sxs-lookup"><span data-stu-id="acf7b-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="acf7b-124">O cliente pode obter ou definir o estado atual do objeto ou descobrir sobre os recursos de retorno de chamada do objeto (chamando **IMAPIOffline:: GetCapabilities** ) e optar por configurar os retornos de chamada usando o **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="acf7b-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="acf7b-125">Um membro desta interface é um espaço reservado reservado para o uso interno do Microsoft Outlook 2013 e está sujeito a alterações.</span><span class="sxs-lookup"><span data-stu-id="acf7b-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="acf7b-126">Outros membros nesta interface devem ser usados apenas conforme documentado.</span><span class="sxs-lookup"><span data-stu-id="acf7b-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="acf7b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="acf7b-127">See also</span></span>



[<span data-ttu-id="acf7b-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="acf7b-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="acf7b-129">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="acf7b-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="acf7b-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="acf7b-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="acf7b-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="acf7b-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

