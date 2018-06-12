---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: dc802d8fef0d90672428c8bfa3662a2734637d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765937"
---
# <a name="iolkaccount"></a>IOlkAccount

Suporte a obtenção e definição de propriedades e outras informações sobre uma conta.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
|Provided by:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) e [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Obtém o tipo e categorias da conta especificada.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Obtém o valor da propriedade conta especificada. Consulte a tabela de propriedades a seguir.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Define o valor da propriedade conta especificada. Consulte a tabela de propriedades a seguir.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Libera memória alocada pela interface **IOlkAccount** .  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Confirma as alterações para o objeto account escrevendo no repositório de registro.  <br/> |
   
## <a name="properties"></a>Propriedades

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa a identificação de entrada da pasta de entrega padrão para a conta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa a identificação de entrada do repositório de entrega padrão para a conta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Retorna o identificador de conta no Outlook 2000 e versões anteriores do Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True se a conta for uma conta do Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Retorna o identificador da conta nas versões do Outlook desde o Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Retorna o nome da conta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera o identificador exclusivo (UID) para a seção de perfil que armazena as preferências de conta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Retorna o carimbo de conta "Enviar".  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa a identificação de entrada da pasta padrão para itens enviados para a conta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Retorna o carimbo da conta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Retorna o nome de exibição do usuário.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica o endereço de email para a conta.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém o UID de uma conta do Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Obtém ou define a identificação de entrada do catálogo de endereços para a conta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa as configurações de transporte que o Microsoft Outlook usa para determinar as tarefas necessárias de sincronização e desabilitar os elementos de interface (UI) do usuário que a conta não oferece suporte.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Esta interface é retornado por **IOlkAccountManager::FindAccount** ao pesquisar uma conta que oferece suporte a **IOlkAccount** e **IOlkEnum::GetNext** quando Obtendo a próxima conta em um enumerador. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

