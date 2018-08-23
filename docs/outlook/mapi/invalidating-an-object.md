---
title: Invalidar um objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566471"
---
# <a name="invalidating-an-object"></a>Invalidar um objeto

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como parte do processo de encerramento do seu provedor, talvez você queira invalidar um objeto. A invalidação de um objeto envolve a substituição seu vtable com uma vtable que contém implementações para os três métodos **IUnknown** : **QueryInterface**, **AddRef**e **Release**. Invalide um objeto chamando [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), um método que está incluído no objeto de suporte de cada um dos três tipos de provedor comuns. Provedores geralmente fazer essa chamada na implementação do método de **Logoff** do objeto seus logon. 
  
A invalidação de um objeto dá MAPI a responsabilidade ultimate para liberar a memória associada ao objeto. Você pode liberar todos os recursos conectados com um objeto e em seguida, chame **MakeInvalid** para invalidar todos os métodos em seus interfaces herdadas. Chamadas para qualquer um desses métodos retornará MAPI_E_INVALID_OBJECT. O uso de **MakeInvalid** é uma opção que muitos provedores de serviço optar por ignorar. 
  
## <a name="see-also"></a>Confira também



[Desligar a um provedor de serviços](shutting-down-a-service-provider.md)

