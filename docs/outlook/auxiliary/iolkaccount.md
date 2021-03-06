---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425061"
---
# <a name="iolkaccount"></a>IOlkAccount

Oferece suporte para obter e definir propriedades e outras informações sobre uma conta.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Provided by:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) e [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Obtém o tipo e as categorias da conta especificada.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Obtém o valor da propriedade de conta especificada. Consulte a tabela Propriedades abaixo.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Define o valor da propriedade de conta especificada. Consulte a tabela Propriedades abaixo.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Libera memória alocada pela interface **IOlkAccount.**  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Confirma as alterações no objeto de conta escrevendo no armazenamento do Registro.  <br/> |
   
## <a name="properties"></a>Propriedades

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa a ID de entrada da pasta de entrega padrão da conta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa a ID de entrada do armazenamento de entrega padrão da conta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Retorna o identificador da conta no Outlook 2000 e em versões anteriores do Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True se a conta for uma conta do Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Retorna o identificador da conta nas versões do Outlook desde o Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Retorna o nome da conta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera o identificador exclusivo (UID) para a seção do perfil que armazena as preferências de conta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Retorna o carimbo "send" da conta.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa a ID de entrada da pasta padrão para itens enviados da conta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Retorna o carimbo de conta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Retorna o nome de exibição do usuário.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica o endereço de email da conta.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém a UID de uma conta do Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Recupera ou define a ID de entrada do catálogo de endereços da conta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa as configurações de transporte que o Microsoft Outlook usa para determinar as tarefas de sincronização necessárias e desabilitar os elementos da interface do usuário aos quais a conta não dá suporte.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa interface é retornada por **IOlkAccountManager::FindAccount** ao procurar uma conta que suporte **IOlkAccount** e **IOlkEnum::GetNext** ao obter a próxima conta em um enumerador. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

