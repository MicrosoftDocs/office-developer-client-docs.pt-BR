---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retorna um identificador que identifica exclusivamente uma conta dentro do perfil na qual a conta é criada.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766058"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Retorna um identificador que identifica exclusivamente uma conta dentro do perfil na qual a conta é criada.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0001  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Marca de propriedade:  <br/> |0x00010003  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md). Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**. 
  
Essa propriedade é diferente do [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) seu valor é exclusivo somente entre todas as contas dentro desse perfil no qual a conta foi criada, enquanto **PROP\_ACCT_MINI_UID** identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada. Quando uma mensagem com essas propriedades se movimenta em um segundo computador com um perfil diferente do Outlook e um conjunto diferente de contas, **PROP_ACCT_ID** possivelmente pode entrar em conflito com uma conta no perfil do segundo computador e **PROP_ACCT_MINI_UID** podem identificar exclusivamente a conta original no perfil original. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

