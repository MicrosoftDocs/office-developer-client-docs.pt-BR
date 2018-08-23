---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565176"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fornece informações adicionais sobre o último erro.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Provided by:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtém uma cadeia de caracteres da mensagem de erro especificado.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa interface fornece informações adicionais sobre um erro em [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)e [IOlkAccount](iolkaccount.md). Também é a interface de base para **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)

