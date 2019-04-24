---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa as configurações de transporte que o Outlook usa para determinar as tarefas de sincronização necessárias e para desabilitar os elementos da interface do usuário que a conta não suporta.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326478"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Representa as configurações de transporte que o Outlook usa para determinar as tarefas de sincronização necessárias e para desabilitar os elementos da interface do usuário que a conta não suporta.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2010  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20100102  <br/> |
|Acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Obter ou definir essa propriedade usando [IOlkAccount:: GetProp](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.
  
Retorna **MAPIACCT_SEND_ONLY** se a conta só puder enviar mensagens, mas não puder receber mensagens. Nesse caso, o Outlook desabilita a IU que não se aplica a esse tipo de conta (por exemplo, a interface do usuário para **Enviar/receber**).
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

