---
title: Implementar uma tabela de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436290"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementar uma tabela de um provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI chama o método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) do provedor quando o usuário de um aplicativo cliente adiciona um destinatário a uma mensagem de saída. Normalmente, os tipos de endereços solicitados são exclusivos do sistema de mensagens. Se o provedor oferecer suporte à criação de destinatários, ele deverá fornecer uma tabela única que exponha modelos para cada tipo de endereço de destinatário suportado. Se o provedor não oferecer suporte à criação de destinatário, retorne MAPI_E_NO_SUPPORT da chamada **GetOneOffTable** . 
  
Normalmente, o MAPI mantém a tabela única do provedor aberta para o tempo de vida da sessão, liberando-o somente quando um cliente chama o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) do subsistema ou do catálogo de endereços. MAPI registra para notificações nesta tabela para que, se os modelos forem adicionados ou excluídos, essas alterações possam ser refletidas para o usuário. 
  
 **Para implementar o IABLogon:: GetOneOffTable**
  
1. Verifique o valor do parâmetro flags, _parâmetroulflags_. Se o sinalizador MAPI_UNICODE estiver definido e seu provedor não oferecer suporte a Unicode, falha e retornar MAPI_E_BAD_CHARWIDTH. 
    
2. Verifique se a tabela única do provedor já foi criada. Como as tabelas únicas são normalmente estáticas, seu provedor nunca precisa passar pelo processo de criação mais de uma vez. Se uma tabela já existir, retorne um ponteiro para ela. 
    
3. Se uma tabela única ainda não existir, chame CreateTable para **** criar uma. 
    
4. Defina as seguintes propriedades para as colunas nas linhas da tabela:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para o nome do tipo de destinatário que o modelo pode criar. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o identificador de entrada para o modelo one-off.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar o nível de hierarquia na exibição da tabela única.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) como true para indicar se a linha representa um modelo e false caso contrário.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço criado pelo modelo.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou outro valor que indica o tipo de exibição do modelo.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) para um valor binário exclusivo. 
    
5. Chame [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) para modificar a tabela diretamente. 
    
6. Call [ITableData:: HrGetView](itabledata-hrgetview.md) criar uma implementação **** de interface IMAPITable para retornar ao chamador. 
    

