---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418047"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="0e9ce-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="0e9ce-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="0e9ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e9ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e9ce-105">Abre uma interface [IMAPIFormMgr](imapiformmgriunknown.md) em um objeto de provedor de biblioteca de formulários no contexto de uma sessão existente.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e9ce-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0e9ce-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e9ce-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="0e9ce-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0e9ce-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0e9ce-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e9ce-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e9ce-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e9ce-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="0e9ce-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e9ce-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0e9ce-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="0e9ce-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e9ce-112">Parameters</span></span>

 <span data-ttu-id="0e9ce-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="0e9ce-113">_pSession_</span></span>
  
> <span data-ttu-id="0e9ce-114">no Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="0e9ce-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="0e9ce-115">_ppmgr_</span></span>
  
> <span data-ttu-id="0e9ce-116">bota Ponteiro para a interface **IMAPIFormMgr** retornada.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e9ce-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0e9ce-117">Return value</span></span>

<span data-ttu-id="0e9ce-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e9ce-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e9ce-119">Remarks</span></span>

<span data-ttu-id="0e9ce-120">Depois que um aplicativo cliente faz uma chamada para a função **MAPIOpenFormMgr** , a maioria das interações relacionadas a formulários subsequentes acontece através do provedor de biblioteca de formulários ou de uma interface retornada pelo provedor de biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="0e9ce-121">A interface **IMAPIFormMgr** permite que o cliente trabalhe com manipuladores de mensagens e execute resoluções entre classes de mensagens e bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e9ce-122">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0e9ce-122">MFCMAPI reference</span></span>

<span data-ttu-id="0e9ce-123">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e9ce-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0e9ce-124">**File**</span></span>|<span data-ttu-id="0e9ce-125">**Função**</span><span class="sxs-lookup"><span data-stu-id="0e9ce-125">**Function**</span></span>|<span data-ttu-id="0e9ce-126">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="0e9ce-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e9ce-127">MainDlg. cpp abre o Gerenciador de formulários para que um formulário possa ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="0e9ce-128">CMainDlg:: OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="0e9ce-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="0e9ce-129">MFCMAPI usa o método **MAPIOpenFormMgr** para abrir o Gerenciador de formulários para que um formulário possa ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e9ce-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e9ce-130">See also</span></span>



[<span data-ttu-id="0e9ce-131">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0e9ce-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

