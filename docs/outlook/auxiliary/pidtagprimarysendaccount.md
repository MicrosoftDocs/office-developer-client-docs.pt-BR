---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica o accountsendstamp principal de uma mensagem.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394080"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Especifica o carimbo “send” de conta principal de uma mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Identificador:  <br/> |0x0E28  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Conta  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade se aplica a um objeto de mensagem MAPI. Para uma mensagem recebida, o carimbo “send” de conta principal indica com qual conta um encaminhamento ou uma resposta deve ser enviada. Para uma mensagem de saída, ele determina com qual conta enviar a mensagem. Seu valor é o valor de [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)
- [Propriedades MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Propriedade canônica PidTagPrimarySendAccount](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

