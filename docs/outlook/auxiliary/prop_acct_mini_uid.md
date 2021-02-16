---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retorna um identificador de conta exclusivo nos perfis do Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409430"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Retorna um identificador de conta exclusivo nos perfis do Outlook.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0003  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Marca de propriedade:  <br/> |0x00030003  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md). Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**. 
  
Essa propriedade é diferente do PROP_ACCT_ID porque seu valor identifica exclusivamente [a](prop_acct_id.md) conta dentro e fora do perfil no qual a conta foi criada, enquanto o PROP_ACCT_ID é exclusivo apenas entre todas as contas nesse perfil em que **a** conta foi criada. Quando uma mensagem com essas propriedades percorre um segundo computador com um perfil do Outlook diferente e um conjunto diferente de contas, o **PROP_ACCT_MINI_UID** pode identificar exclusivamente a conta original no perfil original. No **entanto, PROP_ACCT_ID** pode entrar em conflito com uma conta no perfil do segundo computador. 
  
## <a name="see-also"></a>Confira também

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

