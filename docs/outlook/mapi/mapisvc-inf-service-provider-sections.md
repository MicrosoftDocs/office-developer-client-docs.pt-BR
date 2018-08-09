---
title: Seções do provedor de serviços MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad6a4661025dfd8cbd39d8f58a36d94ab997ada2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768029"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="469c5-103">Seções do provedor de serviços MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="469c5-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="469c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="469c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="469c5-105">Mapisvc inclui uma seção de provedor de serviço para cada uma das entradas listadas na entrada **provedores** na seção anterior de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="469c5-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="469c5-106">Seções do provedor de **serviço** são semelhantes às seções de serviço de mensagem em que os dois tipos de seções contêm entradas neste formato:</span><span class="sxs-lookup"><span data-stu-id="469c5-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="469c5-107">**marca de propriedade** = o valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="469c5-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="469c5-108">No entanto, seções de provedor de serviço e seções de serviço de mensagem diferem tais entradas de propriedade são o único tipo de entrada nas seções do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="469c5-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="469c5-109">Não pode haver nenhum seções adicionais ou vinculadas para provedores de serviços; todas as informações do provedor de serviço devem estar contidas em uma seção.</span><span class="sxs-lookup"><span data-stu-id="469c5-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="469c5-110">Algumas das propriedades definidas nas seções de serviço de mensagem também são definidas nas seções do provedor de serviço, pois essas propriedades fazem sentido para ambos.</span><span class="sxs-lookup"><span data-stu-id="469c5-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="469c5-111">A propriedade **PR_DISPLAY_NAME** é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="469c5-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="469c5-112">Provedores de serviço e serviços de mensagem tem um nome que é usado para exibição na interface do usuário de configuração.</span><span class="sxs-lookup"><span data-stu-id="469c5-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="469c5-113">Dependendo do provedor de serviço, esse nome pode ou não ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="469c5-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="469c5-114">Outras propriedades são específicas para provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="469c5-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="469c5-115">Seções de provedor de serviço típicas incluem as entradas a seguir, que são necessários:</span><span class="sxs-lookup"><span data-stu-id="469c5-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="469c5-116">**PR_DISPLAY_NAME** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="469c5-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="469c5-117">**PR_PROVIDER_DISPLAY** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="469c5-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="469c5-118">**PR_PROVIDER_DLL_NAME** =  _nome do arquivo DLL_</span><span class="sxs-lookup"><span data-stu-id="469c5-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="469c5-119">**PR_RESOURCE_TYPE** =  _longo_</span><span class="sxs-lookup"><span data-stu-id="469c5-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="469c5-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span><span class="sxs-lookup"><span data-stu-id="469c5-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="469c5-121">A entrada **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) é semelhante ao **PR_SERVICE_DLL_NAME**; indica o nome do arquivo para a DLL que contém o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="469c5-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="469c5-122">Código de serviço de mensagem podem ser armazenados sem um dos seus provedores de serviço no mesmo arquivo DLL ou existir como uma DLL separada.</span><span class="sxs-lookup"><span data-stu-id="469c5-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="469c5-123">Observe que nenhum sufixo é incluído na entrada independentemente da plataforma de destino; MAPI cuida de adicionar um sufixo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="469c5-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="469c5-124">**PR_RESOURCE_TYPE** Entrada ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa o tipo de provedor de serviços; provedores de serviços de defini-la como a constante predefinida apropriada.</span><span class="sxs-lookup"><span data-stu-id="469c5-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="469c5-125">Os valores válidos incluem MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER e MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="469c5-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="469c5-126">Outra entrada de propriedade que se aplica aos serviços de mensagem e provedores de serviços, a entrada de **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica as opções.</span><span class="sxs-lookup"><span data-stu-id="469c5-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="469c5-127">As configurações para essa entrada de propriedade diferem, dependendo do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="469c5-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="469c5-128">Por exemplo, alguns provedores de armazenamento de mensagem podem definir **PR_RESOURCE_FLAGS** para STATUS_NO_DEFAULT_STORE se elas nunca poderá operar como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="469c5-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="469c5-129">Três exemplos das seções do provedor de serviço a seguir.</span><span class="sxs-lookup"><span data-stu-id="469c5-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="469c5-130">A seção **[Provedor AB]** é a seção de provedor de serviço para o serviço de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="469c5-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="469c5-131">As seções **[MsgService Prov1]** e **[MsgService Prov2]** pertencem ao My Service próprio; a primeira é uma seção de provedor de catálogo de endereços e o segundo é uma seção de provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="469c5-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


