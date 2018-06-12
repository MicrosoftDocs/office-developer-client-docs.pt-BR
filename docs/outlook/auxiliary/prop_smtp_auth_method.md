---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica o método de autenticação a ser usado para a conta de SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766075"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Especifica o método de autenticação a ser usado para a conta de SMTP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x0208  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x02080003  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Coment�rios

O valor é uma bitmask das seguintes constantes. Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para seus valores. 
  
- **SMTP_AUTH_SAME_AS_POP** significa usando as mesmas credenciais como meu servidor de email de entrada, conforme fornecido pela [PROP_INET_USER](prop_inet_user.md) e [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** significa utilizando as credenciais conforme fornecido pela [PROP_SMTP_USER](prop_smtp_user.md) e [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitando que o usuário para fazer logon no servidor de email de entrada antes de enviar email. 
    
## <a name="see-also"></a>Confira também

- [Gerenciando mensagem downloads para contas POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

