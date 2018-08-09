---
title: Sobre as configurações antispam
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permite que os usuários especifiquem configurações para cada conta para ajudar a proteger a conta contra spam. Tais configurações antispam são armazenadas em uma seção designada para essa conta no perfil do usuário.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765779"
---
# <a name="about-anti-spam-settings"></a>Sobre as configurações antispam

Outlook permite que os usuários especifiquem configurações para cada conta para ajudar a proteger a conta contra spam. Tais configurações antispam são armazenadas em uma seção designada para essa conta no perfil do usuário. Use a propriedade [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obter o ID exclusivo (UID) para a seção no perfil que armazena as preferências do usuário para essa conta, incluindo as configurações antispam. 
  
Use as propriedades a seguir para obter configurações antispam para a conta:
  
- [PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como remetentes bloqueados para a conta.
    
- [PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— Especifica o nível de filtragem de spam que o usuário tiver especificado para a conta. A tabela a seguir mostra os valores com suporte.
    
|Valor com suporte |Definição |
|:-----|:-----|
|Nenhum  <br/> |0xFFFFFFFF  <br/> |
|Baixa  <br/> |0x00000006  <br/> |
|Médio  <br/> |0x00000005  <br/> |
|Alta  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como destinatários confiáveis para a conta.
    
- [PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como remetentes confiáveis para a conta.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)
- [Adicionar os nomes das listas de filtro de lixo eletrônico](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

