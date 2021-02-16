---
title: Recursos do Armazenamento de Mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439517"
---
# <a name="message-store-features"></a>Recursos do Armazenamento de Mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de armazenamento de mensagens são mais complexos do que outros provedores de serviços MAPI em que os provedores de armazenamento de mensagens têm uma ampla variedade de recursos opcionais que podem implementar. A lista de recursos necessários para um provedor de armazenamento de mensagens é bastante curta. No entanto, um provedor de armazenamento de mensagens típico dará suporte a vários recursos opcionais, pois muitos dos recursos opcionais são muito úteis ou exigidos pela maioria dos clientes MAPI. A tabela a seguir lista os principais recursos que os provedores de armazenamento de mensagens podem implementar e se cada recurso é obrigatório ou opcional para todos os provedores de armazenamento de mensagens e para provedores de armazenamento de mensagens padrão.
  
|**Característica**|**Tudo**|**Padrão**|
|:-----|:-----|:-----|
|Fornecendo status com a tabela de status MAPI.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Implementação de objetos de pasta.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Implementar objetos de mensagem.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecer relatórios de leitura e não leitura.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecendo uma interface de progresso.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecendo uma interface de configuração.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Suporte a tabelas de conteúdo associadas para suporte a formulário e exibição.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Enviar mensagens com o provedor do armazenamento de mensagens.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Receber mensagens com o provedor do armazenamento de mensagens.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Suporte a anexos de mensagem.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte ao Formato Rich Text para mensagens.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Fornecendo notificações.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte a pesquisas.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte a provedores de transporte/armazenamento de mensagens fortemente a par.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte à não reutilização de identificadores de entrada.  <br/> |Opcional  <br/> |Opcional  <br/> |
   
Muitos dos recursos opcionais podem ser anunciados para mapi e aplicativos cliente definindo vários sinalizadores na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto de repositório de mensagens. Os recursos necessários não têm sinalizadores associados a eles. **PR_STORE_SUPPORT_MASK** é necessário no armazenamento de mensagens, pasta e objetos de mensagem. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

