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
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586029"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="7ebaa-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="7ebaa-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="7ebaa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ebaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ebaa-105">Abre uma interface de [IMAPIFormMgr](imapiformmgriunknown.md) em um objeto de provedor de biblioteca de formulário no contexto de uma sessão existente.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ebaa-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7ebaa-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ebaa-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="7ebaa-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7ebaa-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7ebaa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7ebaa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7ebaa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7ebaa-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7ebaa-110">Called by:</span></span>  <br/> |<span data-ttu-id="7ebaa-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="7ebaa-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="7ebaa-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ebaa-112">Parameters</span></span>

 <span data-ttu-id="7ebaa-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="7ebaa-113">_pSession_</span></span>
  
> <span data-ttu-id="7ebaa-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="7ebaa-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="7ebaa-115">_ppmgr_</span></span>
  
> <span data-ttu-id="7ebaa-116">[out] Ponteiro para a interface de **IMAPIFormMgr** retornado.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ebaa-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7ebaa-117">Return value</span></span>

<span data-ttu-id="7ebaa-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ebaa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ebaa-119">Remarks</span></span>

<span data-ttu-id="7ebaa-120">Depois que um aplicativo cliente faz uma chamada para a função **MAPIOpenFormMgr** , a maioria das interações subsequentes relacionados a formulários ocorrem por meio do provedor de biblioteca de formulário ou uma interface retornados pelo provedor de biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="7ebaa-121">A interface de **IMAPIFormMgr** permite que o cliente trabalhar com manipuladores de mensagens e executar resoluções entre as classes de mensagem e bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ebaa-122">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7ebaa-122">MFCMAPI reference</span></span>

<span data-ttu-id="7ebaa-123">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ebaa-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7ebaa-124">**File**</span></span>|<span data-ttu-id="7ebaa-125">**Function**</span><span class="sxs-lookup"><span data-stu-id="7ebaa-125">**Function**</span></span>|<span data-ttu-id="7ebaa-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7ebaa-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ebaa-127">MainDlg.cpp abre o Gerenciador de formulário para que um formulário pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="7ebaa-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="7ebaa-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="7ebaa-129">MFCMAPI usa o método **MAPIOpenFormMgr** para abrir o Gerenciador de formulário para que um formulário pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="7ebaa-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ebaa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ebaa-130">See also</span></span>



[<span data-ttu-id="7ebaa-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7ebaa-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

