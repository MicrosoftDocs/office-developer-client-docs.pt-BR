---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586393"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="1783c-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="1783c-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="1783c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1783c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1783c-105">Exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="1783c-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="1783c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1783c-106">Parameters</span></span>

 <span data-ttu-id="1783c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1783c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1783c-108">[in] Uma alça para a janela pai da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="1783c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1783c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1783c-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1783c-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1783c-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="1783c-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="1783c-112">[in] Um ponteiro para o título da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="1783c-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="1783c-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="1783c-114">[in] Um ponteiro para a tabela de exibição que descreve os controles para que ele apareça na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="1783c-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="1783c-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="1783c-116">[in] Um ponteiro para a implementação de [IMAPIProp](imapipropiunknown.md) a ser usado para acessar as propriedades de configuração a ser exibida na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="1783c-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="1783c-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="1783c-118">[in] Um índice baseado em zero à página padrão superior da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1783c-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1783c-119">Return value</span></span>

<span data-ttu-id="1783c-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="1783c-120">S_OK</span></span> 
  
> <span data-ttu-id="1783c-121">A folha de propriedades de configuração foi exibida.</span><span class="sxs-lookup"><span data-stu-id="1783c-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1783c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1783c-122">Remarks</span></span>

<span data-ttu-id="1783c-123">O método **IMAPISupport::DoConfigPropsheet** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="1783c-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="1783c-124">**DoConfigPropSheet** fornece uma interface de usuário padrão para exibir as propriedades de provedores de serviço e serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1783c-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="1783c-125">Você deve usar essa caixa de diálogo padrão para todas as exibições da propriedade de configuração para que os usuários se beneficiam de uma interface consistente do Windows.</span><span class="sxs-lookup"><span data-stu-id="1783c-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="1783c-126">Provedores de serviços de chamarem **DoConfigPropSheet** como parte de sua implementação do método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou com um botão usado para exibir detalhes em Propriedades.</span><span class="sxs-lookup"><span data-stu-id="1783c-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="1783c-127">Serviços de mensagem chamar **DoConfigPropSheet** de seu função de ponto de entrada de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1783c-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1783c-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1783c-128">Notes to callers</span></span>

<span data-ttu-id="1783c-129">Você pode criar a tabela de exibição apontada pelo parâmetro _lpDisplayTable_ chamando a função [BuildDisplayTable](builddisplaytable.md) ou com código personalizado.</span><span class="sxs-lookup"><span data-stu-id="1783c-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1783c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1783c-130">See also</span></span>



[<span data-ttu-id="1783c-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="1783c-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="1783c-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="1783c-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="1783c-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1783c-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="1783c-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1783c-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="1783c-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="1783c-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="1783c-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1783c-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="1783c-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1783c-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="1783c-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="1783c-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="1783c-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1783c-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

