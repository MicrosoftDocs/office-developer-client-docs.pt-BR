---
title: Sobre as configurações antispam
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: O Outlook permite aos usuários especificar configurações para cada conta a fim de protegê-la contra spam. Essas configurações antispam são armazenadas em uma seção designada para essa conta no perfil de usuário.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316956"
---
# <a name="about-anti-spam-settings"></a>Sobre as configurações antispam

O Outlook permite aos usuários especificar configurações para cada conta a fim de protegê-la contra spam. Essas configurações antispam são armazenadas em uma seção designada para essa conta no perfil de usuário. Use a propriedade [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obter a ID exclusiva (UID) da seção no perfil que armazena as preferências do usuário para essa conta, incluindo as configurações antispam. 
  
Use as seguintes propriedades para obter as configurações antispam da conta:
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como remetentes bloqueados da conta.
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx): especifica o nível de filtragem de spam que o usuário especificou para a conta. A tabela a seguir mostra os valores compatíveis.
    
|Valor compatível |Definição |
|:-----|:-----|
|Nenhum  <br/> |0xFFFFFFFF  <br/> |
|Baixo  <br/> |0x00000006  <br/> |
|Médio  <br/> |0x00000005  <br/> |
|Alto  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como destinatários confiáveis da conta.
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como remetentes confiáveis da conta.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)
- [Adicionar nomes às listas de filtros de lixo eletrônico](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

