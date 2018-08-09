---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica o accountsendstamp secundário da mensagem.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766052"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Especifica o carimbo de conta secundária "Enviar" para a mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificador:  <br/> |0x0E29  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade se aplica a um objeto de mensagem MAPI. Para uma mensagem recebida, o carimbo de data / conta secundária "Enviar" indica qual conta um encaminhamento ou uma resposta deve ser enviada com, se o encaminhamento e a resposta não pode ser enviada com a conta principal. Para uma mensagem de saída, a conta secundária "Enviar" carimbo determina com qual conta para enviar a mensagem, se a mensagem não pode ser enviada com a conta principal. Seu valor é o valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface de [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)
- [Propriedades MAPI](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propriedade canônica PidTagNextSendAcct](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

