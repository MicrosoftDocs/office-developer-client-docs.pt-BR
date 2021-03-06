---
title: Propriedades (PI de gerenciamento de contas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: Esta seção descreve as propriedades na API de Gerenciamento de Conta.
ms.openlocfilehash: d0b8c06716bd2f3a3bb2941e098bd9f11ab87183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416332"
---
# <a name="properties-account-management-api"></a>Propriedades (PI de gerenciamento de contas)

Esta seção descreve as propriedades na API de Gerenciamento de Conta.
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Este é o carimbo de "envio" da conta secundária para a mensagem.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Este é o carimbo "send" da conta principal para uma mensagem.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Representa a ID de entrada da pasta de entrega padrão da conta.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Representa a ID de entrada do armazenamento de entrega padrão da conta.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Retorna um identificador que identifica exclusivamente uma conta dentro do perfil no qual a conta é criada.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True se a conta for uma conta do Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Retorna um identificador de conta exclusivo nos perfis do Outlook.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Retorna ou define o nome da conta.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Recupera o identificador exclusivo (UID) para a seção do perfil que armazena as preferências de conta.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Retorna o carimbo "send" da conta.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Representa a ID de entrada da pasta padrão para itens enviados da conta.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Retorna o carimbo de conta.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Especifica o endereço de email da conta.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Retorna ou define o nome de exibição do usuário.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Representa a senha do usuário para uma caixa de correio geral da Internet.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Representa o número da porta de uma caixa de correio geral da Internet.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Representa o nome do servidor de uma caixa de correio geral da Internet.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Especifica se o SSL deve ser usado para uma caixa de correio geral da Internet.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Especifica se a Autenticação de Senha Segura (SPA) deve ser usada para uma caixa de correio geral da Internet.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Representa o nome de usuário de uma caixa de correio geral da Internet.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém a UID de uma conta do Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Recupera ou define a ID de entrada do catálogo de endereços da conta.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Representa as configurações de transporte que o Outlook usa para determinar as tarefas de sincronização necessárias e desabilitar os elementos da interface do usuário aos quais a conta não dá suporte.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Especifica deixar uma cópia de uma mensagem no servidor para uma conta POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Especifica o método de autenticação a ser usado para a conta SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Representa a senha da conta SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Representa o número da porta da conta SMTP.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Especifica o tipo de conexão criptografada a ser usada para uma conta SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Representa o nome do servidor da conta SMTP.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Especifica se o protocolo SSL deve ser usado para a conta SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Especifica se a autenticação deve ser usada para a conta SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Especifica se é para usar a Autenticação de Senha Segura (SPA) para a conta SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Representa o nome de usuário da conta SMTP.  <br/> |
   

