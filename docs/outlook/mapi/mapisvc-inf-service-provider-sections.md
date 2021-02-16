---
title: Seções do Provedor de Serviços MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405559"
---
# <a name="mapisvcinf-service-provider-sections"></a>Seções do Provedor de Serviços MapiSvc.inf

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf inclui uma seção de provedor de serviços para cada uma das entradas listadas na entrada **Provedores** na seção anterior dos serviços de mensagem. **As** seções do provedor de serviços são semelhantes às seções de serviço de mensagens, já que ambos os tipos de seções contêm entradas nesse formato: 
  
**property tag** = property value 
  
No entanto, as seções do provedor de serviços e as seções do serviço de mensagens diferem porque essas entradas de propriedade são o único tipo de entrada incluída nas seções do provedor de serviços. Não pode haver seções adicionais ou vinculadas para provedores de serviços; todas as informações do provedor de serviços devem estar contidas em uma seção. 
  
Algumas das propriedades definidas nas seções do serviço de mensagens também são definidas nas seções do provedor de serviços porque essas propriedades fazem sentido para ambas. A **PR_DISPLAY_NAME** propriedade é um exemplo. Os provedores de serviços e os serviços de mensagens têm um nome que é usado para exibição na interface do usuário de configuração. Dependendo do provedor de serviços, esse nome pode ou não ser o mesmo. Outras propriedades são específicas para provedores de serviços. 
  
As seções típicas do provedor de serviços incluem as seguintes entradas, todas necessárias:
  
**PR_DISPLAY_NAME**  =   _string_
  
**PR_PROVIDER_DISPLAY**  =   _string_
  
**PR_PROVIDER_DLL_NAME**  =   _nome do arquivo DLL_
  
**PR_RESOURCE_TYPE**  =   _long_
  
**PR_RESOURCE_FLAGS**  =   _bitmask_
  
A **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) é semelhante a **PR_SERVICE_DLL_NAME**; ele indica o nome de arquivo para a DLL que contém o provedor de serviços. O código do serviço de mensagens pode ser armazenado com um de seus provedores de serviços no mesmo arquivo DLL ou existir como uma DLL separada. Observe que nenhum sufixo está incluído na entrada, independentemente da plataforma de destino; O MAPI cuida da adição de um sufixo, se necessário. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa o tipo de provedor de serviços; os provedores de serviços a configuram como a constante predefinida apropriada. Os valores válidos incluem MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER e MAPI_AB_PROVIDER.
  
Outra entrada de propriedade que se aplica a serviços de mensagens e provedores de serviços, a entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica opções. As configurações para essa entrada de propriedade podem diferir dependendo do provedor de serviços. Por exemplo, alguns provedores  de armazenamento de mensagens podem definir PR_RESOURCE_FLAGS como STATUS_NO_DEFAULT_STORE se nunca puderem operar como o armazenamento de mensagens padrão. 
  
Três exemplos de seções do provedor de serviços a seguir. A **seção [AB Provider]** é a seção do provedor de serviços para o serviço de Agenda Padrão. As **seções [MsgService Prov1]** e **[MsgService Prov2]** pertencem a Meu Próprio Serviço; a primeira é uma seção de provedor de endereços e a segunda é uma seção de provedor de armazenamento de mensagens. 
  
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


