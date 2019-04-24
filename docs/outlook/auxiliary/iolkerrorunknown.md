---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321851"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fornece informações extras sobre o último erro.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Fornecido por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtém uma cadeia de caracteres de mensagem para o erro especificado.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta interface fornece informações extras sobre um erro no [IOlkAccountManager](iolkaccountmanager.md), no [IOlkAccountNotify](iolkaccountnotify.md)e no [IOlkAccount](iolkaccount.md). Também é a interface base para **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)

