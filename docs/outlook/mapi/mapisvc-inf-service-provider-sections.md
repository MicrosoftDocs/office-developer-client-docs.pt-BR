---
title: Seções do provedor de serviços MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309538"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="5941e-103">Seções do provedor de serviços MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="5941e-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="5941e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5941e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5941e-105">MAPISVC. inf inclui uma seção de provedor de serviços para cada uma das entradas listadas na entrada de **provedores** na seção serviços de mensagem anterior.</span><span class="sxs-lookup"><span data-stu-id="5941e-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="5941e-106">As seções do provedor de **Serviços** são semelhantes às seções do serviço de mensagens em que ambos os tipos de seções contêm entradas neste formato:</span><span class="sxs-lookup"><span data-stu-id="5941e-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="5941e-107">**marca de propriedade** = valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5941e-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="5941e-108">No enTanto, as seções de provedor de serviços e de serviço de mensagens diferem que essas entradas de propriedade são o único tipo de entrada incluído nas seções do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5941e-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="5941e-109">Não pode haver seções adicionais ou vinculadas para provedores de serviços; todas as informações do provedor de serviços devem estar contidas em uma seção.</span><span class="sxs-lookup"><span data-stu-id="5941e-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="5941e-110">Algumas das propriedades definidas nas seções do serviço de mensagens também são definidas nas seções do provedor de serviços porque essas propriedades fazem sentido para ambos.</span><span class="sxs-lookup"><span data-stu-id="5941e-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="5941e-111">A propriedade **PR_DISPLAY_NAME** é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="5941e-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="5941e-112">Os provedores de serviços e serviços de mensagens têm um nome que é usado para exibição na interface do usuário de configuração.</span><span class="sxs-lookup"><span data-stu-id="5941e-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="5941e-113">Dependendo do provedor de serviços, esse nome pode ou não ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="5941e-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="5941e-114">Outras propriedades são específicas dos provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="5941e-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="5941e-115">As seções típicas do provedor de serviços incluem as entradas a seguir, que são necessárias:</span><span class="sxs-lookup"><span data-stu-id="5941e-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="5941e-116">\*\*\*\* =  _Cadeia de caracteres_ PR_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="5941e-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="5941e-117">\*\*\*\* =  _Cadeia de caracteres_ PR_PROVIDER_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="5941e-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="5941e-118">**PR_PROVIDER_DLL_NAME** =  _nome do arquivo dll_</span><span class="sxs-lookup"><span data-stu-id="5941e-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="5941e-119">**PR_RESOURCE_TYPE** =  _Long_</span><span class="sxs-lookup"><span data-stu-id="5941e-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="5941e-120">\*\*\*\* =  _Bitmask_ PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5941e-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="5941e-121">A entrada **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) é semelhante a **PR_SERVICE_DLL_NAME**; Ele indica o nome de arquivo da DLL que contém o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5941e-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="5941e-122">O código de serviço de mensagens pode ser armazenado com um de seus provedores de serviços no mesmo arquivo DLL ou existe como uma DLL separada.</span><span class="sxs-lookup"><span data-stu-id="5941e-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="5941e-123">Observe que nenhum sufixo está incluído na entrada independentemente da plataforma de destino; O MAPI cuida da adição de um sufixo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5941e-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="5941e-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa o tipo de provedor de serviços; os provedores de serviços os definem para a constante predefinida apropriada.</span><span class="sxs-lookup"><span data-stu-id="5941e-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="5941e-125">Os valores válidos incluem MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER e MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="5941e-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="5941e-126">Outra entrada de propriedade que se aplica aos serviços de mensagens e provedores de serviços, a entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica opções.</span><span class="sxs-lookup"><span data-stu-id="5941e-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="5941e-127">As configurações dessa entrada de propriedade podem diferir, dependendo do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5941e-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="5941e-128">Por exemplo, alguns provedores de repositórios de mensagens podem definir **PR_RESOURCE_FLAGS** como STATUS_NO_DEFAULT_STORE se nunca podem operar como o repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="5941e-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="5941e-129">A seguir estão três exemplos de seções do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5941e-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="5941e-130">A seção **[provedor AB]** é a seção de provedor de serviços do serviço de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="5941e-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="5941e-131">As seções **[MsgService Prov1]** e **[MsgService Prov2]** pertencem ao meu próprio serviço; o primeiro é uma seção de provedor de catálogo de endereços e o segundo é uma seção de provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5941e-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


