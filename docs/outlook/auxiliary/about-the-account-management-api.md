---
title: Sobre a API de gerenciamento de contas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'A API de gerenciamento de contas fornece acesso a informações de conta e dá suporte a notificações de alterações de conta. Como clientes desta API, os provedores de email fazem o seguinte:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426246"
---
# <a name="about-the-account-management-api"></a>Sobre a API de gerenciamento de contas

A API de gerenciamento de contas fornece acesso a informações de conta e dá suporte a notificações de alterações de conta. Como clientes desta API, os provedores de email fazem o seguinte:
  
1. Use o [IOlkAccountManager](iolkaccountmanager.md) para gerenciar o acesso a contas e configurar notificações sobre alterações de conta. 
    
2. Implementar e usar o [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificações sobre alterações de conta. 
    
3. Use [IOlkEnum](iolkenum.md) para enumerar contas. 
    
4. Use o [IOlkAccount](iolkaccount.md) para obter e definir propriedades e outras informações sobre uma conta. Os clientes obtêm essa interface por meio do [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum:: GetNext](iolkenum-getnext.md) para acessar uma conta individual. 
    
5. Implementar e usar o [IOlkAccountHelper](iolkaccounthelper.md) para fornecer a funcionalidade auxiliar do gerente de contas, incluindo obter o nome do perfil da conta e a sessão MAPI atual. 
    
6. Implementar e usar o [IOlkErrorUnknown](iolkerrorunknown.md) para fornecer informações adicionais sobre um erro no **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Componentes da API de gerenciamento de contas

A API de gerenciamento de contas fornece as seguintes definições, tipos de dados, interfaces, propriedades nomeadas e propriedades.
  
### <a name="definitions"></a>Definições
  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)
    
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
    

