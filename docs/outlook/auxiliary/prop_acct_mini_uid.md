---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retorna um identificador de conta que seja exclusivo entre perfis do Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766059"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Retorna um identificador de conta que seja exclusivo entre perfis do Outlook.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0003  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Marca de propriedade:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md). Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**. 
  
Essa propriedade é diferente do [PROP_ACCT_ID](prop_acct_id.md) em que seu valor identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada, enquanto **PROP_ACCT_ID** é exclusiva somente entre todas as contas em que um único perfil em que a conta foi criada. Quando uma mensagem com essas propriedades se movimenta em um segundo computador com um perfil diferente do Outlook e um conjunto diferente de contas, **PROP_ACCT_MINI_UID** podem identificar exclusivamente a conta original no perfil original. No entanto, **PROP_ACCT_ID** possivelmente podem entrar em conflito com uma conta no perfil do segundo computador. 
  
## <a name="see-also"></a>Confira também

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

