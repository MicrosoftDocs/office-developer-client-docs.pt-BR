---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d7e3e89f15b1bc08c7ce9faab0d0a6326300e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767232"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="62dd8-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="62dd8-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="62dd8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62dd8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62dd8-105">Cria um objeto de suporte de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="62dd8-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="62dd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62dd8-106">Parameters</span></span>

 <span data-ttu-id="62dd8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62dd8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="62dd8-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62dd8-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="62dd8-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="62dd8-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="62dd8-110">[out] Um ponteiro para um ponteiro para o novo objeto de suporte de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="62dd8-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62dd8-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="62dd8-111">Return value</span></span>

<span data-ttu-id="62dd8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="62dd8-112">S_OK</span></span> 
  
> <span data-ttu-id="62dd8-113">O objeto de configuração de suporte foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="62dd8-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62dd8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62dd8-114">Remarks</span></span>

<span data-ttu-id="62dd8-115">O método **IMAPISupport::GetSvcConfigSupportObj** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="62dd8-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="62dd8-116">Provedores de serviços de chamarem **GetSvcConfigSupportObj** para criar um objeto de configuração de suporte a serem passados para uma função de ponto de entrada de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="62dd8-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="62dd8-117">Uma função de ponto de entrada de serviço de mensagem se baseia em protótipo [MSGSERVICEENTRY](msgserviceentry.md) e é chamada pelo métodos da interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="62dd8-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="62dd8-118">Uma função de ponto de entrada de serviço de mensagens permite que os serviços de mensagens configurar sozinhos ou executar outras ações quando o perfil é alterado.</span><span class="sxs-lookup"><span data-stu-id="62dd8-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="62dd8-119">Ponto de entrada de serviço de mensagem funções podem suportar as alterações de configuração, exibindo uma folha de propriedades ou por meio de uma matriz de valores de propriedade é passado para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="62dd8-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62dd8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="62dd8-120">See also</span></span>



[<span data-ttu-id="62dd8-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62dd8-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="62dd8-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="62dd8-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="62dd8-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="62dd8-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="62dd8-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62dd8-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="62dd8-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="62dd8-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="62dd8-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="62dd8-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

