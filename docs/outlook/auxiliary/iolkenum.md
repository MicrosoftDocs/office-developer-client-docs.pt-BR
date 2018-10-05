---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389733"
---
# <a name="iolkenum"></a>IOlkEnum

Suporta enumerando contas como objetos [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Provided by:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtém o número de contas no enumerador.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Redefine o enumerador para o início.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtém a próxima conta no enumerador.  <br/> |
|[Ignorar](iolkenum-skip.md) <br/> |Ignora um número especificado de contas do enumerador.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta interface é retornado por **IOlkAccountManager::EnumerateAccounts** ao obter um enumerador de contas. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

