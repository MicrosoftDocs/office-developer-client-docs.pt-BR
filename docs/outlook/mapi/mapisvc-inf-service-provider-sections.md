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
# <a name="mapisvcinf-service-provider-sections"></a>Seções do provedor de serviços MapiSvc. inf

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPISVC. inf inclui uma seção de provedor de serviços para cada uma das entradas listadas na entrada de **provedores** na seção serviços de mensagem anterior. As seções do provedor de **Serviços** são semelhantes às seções do serviço de mensagens em que ambos os tipos de seções contêm entradas neste formato: 
  
**marca de propriedade** = valor da propriedade 
  
No enTanto, as seções de provedor de serviços e de serviço de mensagens diferem que essas entradas de propriedade são o único tipo de entrada incluído nas seções do provedor de serviços. Não pode haver seções adicionais ou vinculadas para provedores de serviços; todas as informações do provedor de serviços devem estar contidas em uma seção. 
  
Algumas das propriedades definidas nas seções do serviço de mensagens também são definidas nas seções do provedor de serviços porque essas propriedades fazem sentido para ambos. A propriedade **PR_DISPLAY_NAME** é um exemplo. Os provedores de serviços e serviços de mensagens têm um nome que é usado para exibição na interface do usuário de configuração. Dependendo do provedor de serviços, esse nome pode ou não ser o mesmo. Outras propriedades são específicas dos provedores de serviços. 
  
As seções típicas do provedor de serviços incluem as entradas a seguir, que são necessárias:
  
**** =  _Cadeia de caracteres_ PR_DISPLAY_NAME
  
**** =  _Cadeia de caracteres_ PR_PROVIDER_DISPLAY
  
**PR_PROVIDER_DLL_NAME** =  _nome do arquivo dll_
  
**PR_RESOURCE_TYPE** =  _Long_
  
**** =  _Bitmask_ PR_RESOURCE_FLAGS
  
A entrada **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) é semelhante a **PR_SERVICE_DLL_NAME**; Ele indica o nome de arquivo da DLL que contém o provedor de serviços. O código de serviço de mensagens pode ser armazenado com um de seus provedores de serviços no mesmo arquivo DLL ou existe como uma DLL separada. Observe que nenhum sufixo está incluído na entrada independentemente da plataforma de destino; O MAPI cuida da adição de um sufixo, se necessário. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) representa o tipo de provedor de serviços; os provedores de serviços os definem para a constante predefinida apropriada. Os valores válidos incluem MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER e MAPI_AB_PROVIDER.
  
Outra entrada de propriedade que se aplica aos serviços de mensagens e provedores de serviços, a entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica opções. As configurações dessa entrada de propriedade podem diferir, dependendo do provedor de serviços. Por exemplo, alguns provedores de repositórios de mensagens podem definir **PR_RESOURCE_FLAGS** como STATUS_NO_DEFAULT_STORE se nunca podem operar como o repositório de mensagens padrão. 
  
A seguir estão três exemplos de seções do provedor de serviços. A seção **[provedor AB]** é a seção de provedor de serviços do serviço de catálogo de endereços padrão. As seções **[MsgService Prov1]** e **[MsgService Prov2]** pertencem ao meu próprio serviço; o primeiro é uma seção de provedor de catálogo de endereços e o segundo é uma seção de provedor de repositório de mensagens. 
  
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


