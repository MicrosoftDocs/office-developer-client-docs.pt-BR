---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica o accountsendstamp principal de uma mensagem.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766046"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Especifica o carimbo de "Enviar" da conta principal para uma mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Identificador:  <br/> |0x0E28  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Conta  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade se aplica a um objeto de mensagem MAPI. Para uma mensagem recebida, o carimbo de "Enviar" da conta principal indica qual conta um encaminhamento ou uma resposta deve ser enviada com. Para uma mensagem de saída, ele determina qual conta para enviar a mensagem com. Seu valor é o valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface de [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada. 
  
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)
- [Propriedades MAPI](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Propriedade canônico de PidTagPrimarySendAccount](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

