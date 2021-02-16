---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retorna um identificador que identifica exclusivamente uma conta dentro do perfil no qual a conta é criada.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407162"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Retorna um identificador que identifica exclusivamente uma conta dentro do perfil no qual a conta é criada.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0001  <br/> |
|Tipo de propriedade:  <br/> |PT_LONG  <br/> |
|Marca de propriedade:  <br/> |0x00010003  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md). Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**. 
  
Essa propriedade é diferente do [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) porque seu valor é exclusivo apenas entre todas as contas nesse perfil em que a conta foi criada, enquanto o PROP ACCT_MINI_UID identifica exclusivamente a conta dentro e fora do perfil em que **\_ a** conta foi criada. Quando uma mensagem com essas propriedades percorre um segundo computador com um perfil do Outlook diferente e um conjunto diferente de contas, o **PROP_ACCT_ID** pode entrar em conflito com uma conta no perfil do segundo computador e o **PROP_ACCT_MINI_UID** pode identificar exclusivamente a conta original no perfil original. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)  
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

