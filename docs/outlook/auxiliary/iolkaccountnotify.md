---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412496"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fornece um retorno de chamada para o cliente para alterações em uma conta.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Fornecido por:  <br/> | Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |Notifica o cliente sobre as alterações na conta especificada.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta interface é passada para [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md) ao configurar notificações. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

