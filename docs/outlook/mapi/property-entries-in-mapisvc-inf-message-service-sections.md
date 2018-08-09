---
title: Entradas de propriedades nas seções do serviço de mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30f5e0b59bacfab91a3a6c77c0b345d6299df9e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770180"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entradas de propriedades nas seções do serviço de mensagens MapiSvc.inf

  
  
**Aplica-se a**: Outlook 
  
Entradas de definir propriedades usam o seguinte formato:
  
 **marca de propriedade** **=** o valor da propriedade 
  
A marca de propriedade pode ser uma marca de propriedade MAPI padrão se os dados de configuração representam uma das propriedades predefinidas pelo MAPI ou uma marca de não-padrão se os dados não representam uma propriedade MAPI. A marca de não-padrão é feita, combinando o valor de um identificador de propriedade com um tipo de propriedade. O resultado é um número hexadecimal de 8 dígitos. O valor da propriedade pode ser qualquer item faz sentido para a marca de propriedade. 
  
Seções do serviço de mensagem podem conter várias entradas, dependendo do serviço de mensagem que está sendo configurado. Normalmente, as seguintes propriedades MAPI são incluídas em uma seção de serviços de mensagem no formato listado:
  
 **PR_DISPLAY_NAME** =  _cadeia de caracteres_
  
 **PR_SERVICE_DLL_NAME** =  _nome do arquivo DLL_
  
 **PR_SERVICE_ENTRY_NAME** =  _nome da função de ponto de entrada_
  
 **PR_SERVICE_SUPPORT_FILES** =  _lista de arquivos_
  
 **PR_SERVICE_DELETE_FILES** =  _lista de arquivos_
  
 **PR_RESOURCE_FLAGS** =  _bitmask_
  
A cadeia de caracteres **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o nome do serviço na mensagem que é mostrado na interface do usuário, o nome que o usuário associa o serviço de mensagem. O nome de exibição é uma entrada opcional em MAPISVC. Em alguns casos, o nome para exibição será composto de duas partes; uma parte atribuído pelo serviço de mensagem e uma parte atribuído pelo usuário. Se o usuário é responsável pela atribuição de uma das partes, isso normalmente é tratado com uma caixa de diálogo especial conhecida como uma folha de propriedades fornecida pelo serviço de mensagem sob o controle de um aplicativo cliente. 
  
As informações fornecidas para a entrada de **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) são o nome da DLL que contém o serviço de mensagem. As informações fornecidas para a entrada de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) são o nome da função de ponto de entrada dentro desse DLL que chamadas MAPI para configurar o serviço de mensagem. 
  
Os arquivos listados na entrada **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) são arquivos que devem ser instalados com o serviço de mensagem. Da mesma forma, os arquivos na entrada **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) devem ser removidos quando o serviço de mensagem é removido. 
  
A entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) é uma coleção das opções definidas para o serviço de mensagem. Por exemplo, o bit SERVICE_SINGLE_COPY é definido quando o serviço de mensagem pode aparecer apenas uma vez em um determinado perfil. SERVICE_NO_PRIMARY_IDENTITY estará definido o bit é definido se o serviço de mensagem não fornece informações de identidade. 
  
Siga a dois exemplos de entradas de propriedade não-padrão. A primeira entrada especifica o caminho para o arquivo usado pelo catálogo de endereços padrão como o valor da propriedade; a segunda entrada especifica um valor de propriedade numéricos. As duas entradas têm significado específico ao serviço de mensagens de AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


