---
title: Recursos do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 092cf56aea2e246fbb7ef2016a2662a1f67f889b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356900"
---
# <a name="message-store-features"></a>Recursos do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositório de mensagens são mais complexos do que outros provedores de serviço MAPI em que os provedores de repositórios de mensagens têm uma variedade maior de recursos opcionais que podem implementar. A lista de recursos necessários para um provedor de armazenamento de mensagens é bem curta. No enTanto, um provedor de armazenamento de mensagens típico oferecerá suporte a vários recursos opcionais, porque muitos dos recursos opcionais são muito úteis ou necessários para a maioria dos clientes MAPI. A tabela a seguir lista os principais recursos que os provedores de repositório de mensagens podem implementar e se cada recurso é obrigatório ou opcional para todos os provedores de repositórios de mensagens e para os provedores de repositórios de mensagens padrão.
  
|**Recurso**|**All**|**Default**|
|:-----|:-----|:-----|
|Fornecimento de status com a tabela de status MAPI.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Implementar objetos Folder.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Implementar objetos de mensagem.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecer relatórios de leitura e não leitura.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecimento de uma interface de progresso.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Fornecimento de uma interface de configuração.  <br/> |Obrigatório  <br/> |Obrigatório  <br/> |
|Suporte a tabelas de conteúdo associado para o suporte de formulário e exibição.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Envio de mensagens com o provedor de armazenamento de mensagens.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Receber mensagens com o provedor de armazenamento de mensagens.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Suporte a anexos de mensagens.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte para o formato Rich Text para mensagens.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Fornecer notificações.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte a pesquisas.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte a provedores de armazenamento/transporte de mensagens rigidamente acoplados.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte à não-reutilização de identificadores de entrada.  <br/> |Opcional  <br/> |Opcional  <br/> |
   
Muitos dos recursos opcionais podem ser anunciados para aplicativos de MAPI e cliente por meio da definição de vários sinalizadores na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto de repositório de mensagens. Os recursos necessários não têm sinalizadores associados a eles. **PR_STORE_SUPPORT_MASK** é necessário em objetos de mensagens, pastas e repositório de mensagens. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

