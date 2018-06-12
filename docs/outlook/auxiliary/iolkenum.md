---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765995"
---
# <a name="iolkenum"></a>IOlkEnum

Suporta enumerando contas como objetos [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) . 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
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
   
## <a name="remarks"></a>Coment�rios

Esta interface é retornado por **IOlkAccountManager::EnumerateAccounts** ao obter um enumerador de contas. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

