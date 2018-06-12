---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa as configurações de transporte que o Outlook usa para determinar as tarefas necessárias de sincronização e desabilitar os elementos de interface (UI) do usuário que a conta não oferece suporte.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766061"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Representa as configurações de transporte que o Outlook usa para determinar as tarefas necessárias de sincronização e desabilitar os elementos de interface (UI) do usuário que a conta não oferece suporte.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2010  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20100102  <br/> |
|Access:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Coment�rios

Obter ou definir essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.
  
Retorna **MAPIACCT_SEND_ONLY** se a conta só pode enviar mensagens, mas não pode receber mensagens. Nesse caso, Outlook desabilita a interface do usuário que não se aplica a esse tipo de contas (por exemplo, a interface do usuário para **Envio/recebimento**).
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

