---
title: Implementando uma tabela de One-Off provedor
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
# <a name="implementing-a-provider-one-off-table"></a>Implementando uma tabela de One-Off provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI chama o método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) do provedor quando o usuário de um aplicativo cliente adiciona um destinatário a uma mensagem de saída. Normalmente, os tipos de endereços solicitados são exclusivos do sistema de mensagens. Se seu provedor oferece suporte à criação de destinatários, ele deve fornecer uma tabela única que expõe modelos para cada tipo de endereço de destinatário com suporte. Se o provedor não suportar a criação de destinatários, retorne MAPI_E_NO_SUPPORT da **chamada GetOneOffTable.** 
  
O MAPI normalmente manterá a tabela única do provedor aberta durante a sessão, liberando-a somente quando um cliente chamar o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do subsistema ou do livro de endereços. MapI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user. 
  
 **Para implementar IABLogon::GetOneOffTable**
  
1. Verifique o valor do parâmetro flags,  _ulFlags_. Se o MAPI_UNICODE sinalizador estiver definido e seu provedor não suportar Unicode, falhará e retornará MAPI_E_BAD_CHARWIDTH. 
    
2. Verifique se a tabela única do provedor já foi criada. Como as tabelas one-off são normalmente estáticas, seu provedor nunca precisa passar pelo processo de criação mais de uma vez. Se uma tabela já existir, retorne um ponteiro para ela. 
    
3. Se uma tabela única ainda não existir, chame **CreateTable** para criar uma. 
    
4. De definidas as seguintes propriedades para as colunas em suas linhas de tabela:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para o nome do tipo de destinatário que o modelo pode criar. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o identificador de entrada para o modelo único.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar o nível de hierarquia na exibição de tabela única.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) como TRUE para indicar se a linha representa um modelo e FALSE caso contrário.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço criado pelo modelo.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER ou outro valor que indique o tipo de exibição para o modelo.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) para um valor binário exclusivo. 
    
5. Chame [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar a tabela diretamente. 
    
6. Chame [ITableData::HrGetView](itabledata-hrgetview.md) para criar uma implementação de interface **IMAPITable** para retornar ao chamador. 
    

