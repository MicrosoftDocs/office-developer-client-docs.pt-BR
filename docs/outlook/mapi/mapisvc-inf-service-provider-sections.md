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
# <a name="mapisvcinf-service-provider-sections"></a>Seções do provedor de serviços MapiSvc.inf

**Aplica-se a**: Outlook 
  
Mapisvc inclui uma seção de provedor de serviço para cada uma das entradas listadas na entrada **provedores** na seção anterior de serviços de mensagem. Seções do provedor de **serviço** são semelhantes às seções de serviço de mensagem em que os dois tipos de seções contêm entradas neste formato: 
  
**marca de propriedade** = o valor da propriedade 
  
No entanto, seções de provedor de serviço e seções de serviço de mensagem diferem tais entradas de propriedade são o único tipo de entrada nas seções do provedor de serviço. Não pode haver nenhum seções adicionais ou vinculadas para provedores de serviços; todas as informações do provedor de serviço devem estar contidas em uma seção. 
  
Algumas das propriedades definidas nas seções de serviço de mensagem também são definidas nas seções do provedor de serviço, pois essas propriedades fazem sentido para ambos. A propriedade **PR_DISPLAY_NAME** é um exemplo. Provedores de serviço e serviços de mensagem tem um nome que é usado para exibição na interface do usuário de configuração. Dependendo do provedor de serviço, esse nome pode ou não ser os mesmos. Outras propriedades são específicas para provedores de serviços. 
  
Seções de provedor de serviço típicas incluem as entradas a seguir, que são necessários:
  
**PR_DISPLAY_NAME** =  _cadeia de caracteres_
  
**PR_PROVIDER_DISPLAY** =  _cadeia de caracteres_
  
**PR_PROVIDER_DLL_NAME** =  _nome do arquivo DLL_
  
**PR_RESOURCE_TYPE** =  _longo_
  
**PR_RESOURCE_FLAGS** =  _bitmask_
  
A entrada **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) é semelhante ao **PR_SERVICE_DLL_NAME**; indica o nome do arquivo para a DLL que contém o provedor de serviço. Código de serviço de mensagem podem ser armazenados sem um dos seus provedores de serviço no mesmo arquivo DLL ou existir como uma DLL separada. Observe que nenhum sufixo é incluído na entrada independentemente da plataforma de destino; MAPI cuida de adicionar um sufixo, se necessário. 
  
**PR_RESOURCE_TYPE** Entrada ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa o tipo de provedor de serviços; provedores de serviços de defini-la como a constante predefinida apropriada. Os valores válidos incluem MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER e MAPI_AB_PROVIDER.
  
Outra entrada de propriedade que se aplica aos serviços de mensagem e provedores de serviços, a entrada de **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica as opções. As configurações para essa entrada de propriedade diferem, dependendo do provedor de serviço. Por exemplo, alguns provedores de armazenamento de mensagem podem definir **PR_RESOURCE_FLAGS** para STATUS_NO_DEFAULT_STORE se elas nunca poderá operar como o armazenamento de mensagens padrão. 
  
Três exemplos das seções do provedor de serviço a seguir. A seção **[Provedor AB]** é a seção de provedor de serviço para o serviço de catálogo de endereços padrão. As seções **[MsgService Prov1]** e **[MsgService Prov2]** pertencem ao My Service próprio; a primeira é uma seção de provedor de catálogo de endereços e o segundo é uma seção de provedor de armazenamento de mensagens. 
  
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


