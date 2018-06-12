---
title: Sobre a API de gerenciamento de conta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'A API de gerenciamento de conta fornece acesso às informações de conta e dá suporte a notificações de alterações de conta. Como os clientes desta API, provedores de email faça o seguinte:'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765789"
---
# <a name="about-the-account-management-api"></a>Sobre a API de gerenciamento de conta

A API de gerenciamento de conta fornece acesso às informações de conta e dá suporte a notificações de alterações de conta. Como os clientes desta API, provedores de email faça o seguinte:
  
1. Use [IOlkAccountManager](iolkaccountmanager.md) para gerenciar o acesso às contas e configurar notificações sobre alterações de conta. 
    
2. Implementar e usar [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificações sobre alterações de conta. 
    
3. Use [IOlkEnum](iolkenum.md) para enumerar contas. 
    
4. Use [IOlkAccount](iolkaccount.md) para obter e definir propriedades e outras informações sobre uma conta. Os clientes obtêm essa interface por meio de [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum::GetNext](iolkenum-getnext.md) para acessar uma conta individual. 
    
5. Implementar e usar [IOlkAccountHelper](iolkaccounthelper.md) para fornecer a funcionalidade de auxiliares do Gerenciador conta, incluindo obtendo o nome do perfil da conta e a sessão MAPI atual. 
    
6. Implementar e usar [IOlkErrorUnknown](iolkerrorunknown.md) para fornecer informações adicionais sobre um erro em **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Componentes de API de gerenciamento de conta

A API de gerenciamento de conta fornece as seguintes definições, tipos de dados, interfaces, denominadas propriedades e propriedades.
  
### <a name="definitions"></a>Definições
  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)
    
### <a name="data-types"></a>Tipos de dados
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>Interfaces
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>Propriedades nomeadas
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>Propriedades
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

