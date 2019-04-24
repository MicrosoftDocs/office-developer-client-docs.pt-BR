---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica o tipo de conexão criptografada a ser usada para uma conta SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328326"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Especifica o tipo de conexão criptografada a ser usada para uma conta SMTP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x020A  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x020A0003  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

O valor pode ser uma das seguintes constantes. ConFira [constantes (API de gerenciamento de contas)](constants-account-management-api.md) para seus valores. 
  
|**Constants**|**Descrição**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Não use nenhuma criptografia.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Use a criptografia SSL (Secure Socket Layer).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Use o protocolo de autenticação e criptografia TLS (Transport Layer Security).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Detectar e usar automaticamente o método de criptografia suportado pelo servidor de email.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

