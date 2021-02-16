---
title: Entradas de propriedade em Seções do Serviço de Mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427994"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entradas de propriedade em Seções do Serviço de Mensagens MapiSvc.inf

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Entradas que configuram propriedades usam esse formato:
  
 **marca de propriedade** **=** valor da propriedade 
  
A marca de propriedade poderá ser uma marca de propriedade MAPI padrão se os dados de configuração representarem uma das propriedades predefinidos por MAPI ou uma marca não padrão se os dados não representarem uma propriedade MAPI. A marca não padrão é feita combinando o valor de um identificador de propriedade com um tipo de propriedade. O resultado é um número hexadecimal de 8 dígitos. O valor da propriedade pode ser o que faz sentido para a marca de propriedade. 
  
As seções do serviço de mensagens podem conter uma variedade de entradas, dependendo do serviço de mensagens que está sendo configurado. As seguintes propriedades MAPI são normalmente incluídas em uma seção de serviços de mensagens no formato listado:
  
 **PR_DISPLAY_NAME**  =   _string_
  
 **PR_SERVICE_DLL_NAME**  =   _nome do arquivo DLL_
  
 **PR_SERVICE_ENTRY_NAME**  =   _nome da função de ponto de entrada_
  
 **PR_SERVICE_SUPPORT_FILES**  =   _lista de arquivos_
  
 **PR_SERVICE_DELETE_FILES**  =   _lista de arquivos_
  
 **PR_RESOURCE_FLAGS**  =   _bitmask_
  
A **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o nome do serviço de mensagem que é mostrado na interface do usuário, o nome que o usuário associa ao serviço de mensagens. O nome de exibição é uma entrada opcional em mapisvc.inf. Às vezes, o nome de exibição será feito de duas partes; uma parte atribuída pelo serviço de mensagens e uma parte atribuída pelo usuário. Se o usuário for responsável pela atribuição de uma das partes, isso geralmente será tratado com uma caixa de diálogo especial conhecida como folha de propriedades fornecida pelo serviço de mensagens sob o controle de um aplicativo cliente. 
  
As informações fornecidas para **a PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) são o nome da DLL que contém o serviço de mensagem. As informações fornecidas para a entrada **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) é o nome da função de ponto de entrada dentro dessa DLL que MAPI chama para configurar o serviço de mensagem. 
  
Os arquivos listados **na PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) são arquivos que devem ser instalados com o serviço de mensagens. Da mesma forma, os arquivos na **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) devem ser removidos quando o serviço de mensagens for removido. 
  
A **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) é uma coleção de opções definidas para o serviço de mensagens. Por exemplo, o SERVICE_SINGLE_COPY bit é definido quando o serviço de mensagens só pode aparecer uma vez em um determinado perfil. O SERVICE_NO_PRIMARY_IDENTITY bit será definido se o serviço de mensagens não fornecer informações de identidade. 
  
Seguem dois exemplos de entradas de propriedade não padrão. A primeira entrada especifica o caminho para o arquivo usado pelo Livro de Endereços Padrão como o valor da propriedade; a segunda entrada especifica um valor de propriedade numérica. Ambas as entradas têm significado específico para o serviço de mensagens AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


