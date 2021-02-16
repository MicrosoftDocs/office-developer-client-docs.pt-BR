---
title: Invalidando um objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407673"
---
# <a name="invalidating-an-object"></a>Invalidando um objeto

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como parte do processo de desligamento do provedor, talvez você queira invalidar um objeto. Invalidar um objeto envolve substituir sua vtable por uma vtable que contém implementações para os três métodos **IUnknown:** **AddRef**, **Release** e **QueryInterface**. Invalide um objeto chamando [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), um método incluído no objeto de suporte de cada um dos três tipos de provedores comuns. Os provedores geralmente fazem essa chamada na implementação do método **Logoff** do objeto de logon. 
  
Invalidar um objeto oferece ao MAPI a responsabilidade final por liberar a memória associada a um objeto. Você pode liberar todos os recursos conectados a um objeto e chamar **MakeInvalid** para invalidar todos os métodos em suas interfaces herdadas. Chamadas para qualquer um desses métodos retornarão MAPI_E_INVALID_OBJECT. Usar **MakeInvalid** é uma opção que muitos provedores de serviços optam por ignorar. 
  
## <a name="see-also"></a>Confira também



[Desligar um provedor de serviços](shutting-down-a-service-provider.md)

