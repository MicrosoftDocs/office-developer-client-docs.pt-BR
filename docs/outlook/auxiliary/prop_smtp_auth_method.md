---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica o método de autenticação a ser usado para a conta SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434638"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Especifica o método de autenticação a ser usado para a conta SMTP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x0208  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x02080003  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

O valor é uma bitmask das constantes a seguir. ConFira [constantes (API de gerenciamento de contas)](constants-account-management-api.md) para seus valores. 
  
- **SMTP_AUTH_SAME_AS_POP** significa usar as mesmas credenciais que meu servidor de email de entrada, conforme fornecido por [PROP_INET_USER](prop_inet_user.md) e [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** significa usar as credenciais conforme fornecido por [PROP_SMTP_USER](prop_smtp_user.md) e [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitar que o usuário faça logon no servidor de email de entrada antes de enviar email. 
    
## <a name="see-also"></a>Confira também

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

