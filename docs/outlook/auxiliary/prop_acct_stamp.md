---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Retorna o carimbo da conta.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766068"
---
# <a name="propacctstamp"></a>PROP_ACCT_STAMP

Retorna o carimbo da conta.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000D  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Marca de propriedade:  <br/> |0x000D001F  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Coment�rios

Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md). Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

