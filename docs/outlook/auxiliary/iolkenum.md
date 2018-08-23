---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592686"
---
# <a name="iolkenum"></a>IOlkEnum

Suporta enumerando contas como objetos [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
|Provided by:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
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

