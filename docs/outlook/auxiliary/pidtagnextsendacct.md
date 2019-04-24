---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica o accountsendstamp secundário de uma mensagem.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327710"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Especifica o carimbo “send” de conta secundário de uma mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificador:  <br/> |0x0E29  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade se aplica a um objeto de mensagem MAPI. Para uma mensagem recebida, o carimbo “send” de conta principal indica com qual conta será preciso enviar um encaminhamento ou uma resposta se não puder ser enviado com a conta principal. Para uma mensagem de saída, o carimbo “send” de conta secundária determina com qual conta será preciso enviar a mensagem se não puder ser enviada com a conta principal. Seu valor é o valor de [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)
- [Propriedades MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propriedade canônica PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

