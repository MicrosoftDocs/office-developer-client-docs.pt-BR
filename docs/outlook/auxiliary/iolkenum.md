---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322096"
---
# <a name="iolkenum"></a>IOlkEnum

Oferece suporte à enumeração de contas como objetos [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Provided by:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtém o número de contas no enumerador.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Redefine o enumerador para o início.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtém a próxima conta no enumerador.  <br/> |
|[Ignorar](iolkenum-skip.md) <br/> |Ignora um número especificado de contas no enumerador.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa interface é retornada por **IOlkAccountManager:: EnumerateAccounts** ao obter um enumerador de contas. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

