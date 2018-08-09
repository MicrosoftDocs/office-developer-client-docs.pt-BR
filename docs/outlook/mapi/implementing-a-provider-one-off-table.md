---
title: Implementar a tabela única de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767415"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementar a tabela única de um provedor

  
  
**Aplica-se a**: Outlook 
  
MAPI chama o método de [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) do seu provedor quando o usuário de um aplicativo cliente adiciona um destinatário a uma mensagem de saída. Normalmente, os tipos de endereços solicitados são exclusivos para seu sistema de mensagens. Se seu provedor de suporte para a criação de destinatário, ele deve fornecer uma tabela único que expõe os modelos para cada tipo de endereço do destinatário com suporte. Se seu provedor não oferece suporte a criação de destinatário, retorne MAPI_E_NO_SUPPORT da chamada **GetOneOffTable** . 
  
MAPI normalmente será mantenha tabela únicos do seu provedor aberto para o tempo de vida da sessão, liberá-lo apenas quando um cliente chama do subsistema ou método de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do catálogo de endereços. MAPI registra para notificações sobre esta tabela para que se modelos são adicionados ou excluídos, essas alterações podem sejam refletidas ao usuário. 
  
 **Para implementar IABLogon:: GetOneOffTable**
  
1. Verifica o valor do parâmetro flags, _ulFlags_. Se o sinalizador MAPI_UNICODE está definido e o provedor não oferece suporte a Unicode, falhar e retornar MAPI_E_BAD_CHARWIDTH. 
    
2. Verifique se tabela únicos do seu provedor já foi criada. Como tabelas únicas são geralmente estáticas, seu provedor nunca deve passar o processo de criação mais de uma vez. Se já existir uma tabela, retorne um ponteiro para ele. 
    
3. Se ainda não existir uma tabela único, chame **CreateTable** para criar um. 
    
4. Defina as seguintes propriedades para as colunas em suas linhas da tabela:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do tipo de destinatário que o modelo pode criar. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o identificador de entrada para o modelo único.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar o nível de hierarquia na tabela únicas são exibidas.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) como TRUE para indicar se a linha representa um modelo e FALSE caso contrário.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço criado pelo modelo.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou outro valor que indica o tipo de exibição para o modelo.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como um valor binário exclusivo. 
    
5. Chame [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar a tabela diretamente. 
    
6. Chame [ITableData::HrGetView](itabledata-hrgetview.md) para criar uma implementação de interface **IMAPITable** para retornar ao chamador. 
    

