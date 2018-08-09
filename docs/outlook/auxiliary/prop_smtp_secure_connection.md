---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica o tipo de conexão criptografada a ser usado para uma conta de SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766071"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Especifica o tipo de conexão criptografada a ser usado para uma conta de SMTP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x020A  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

O valor pode ser uma das constantes a seguir. Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para seus valores. 
  
|**Constantes**|**Descrição**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Não use qualquer criptografia.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Use a criptografia de camada de soquete seguro (SSL).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Use o protocolo de autenticação e criptografia de segurança de camada de transporte (TLS).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Detectar automaticamente e usar o método de criptografia suportado pelo servidor de email.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

