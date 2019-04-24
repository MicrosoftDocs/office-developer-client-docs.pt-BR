---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa a identificação de entrada da pasta padrão para itens enviados para a conta.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327584"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Representa a identificação de entrada da pasta padrão para itens enviados para a conta. 
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0020  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x00200102  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
A pasta padrão para itens enviados é **itens enviados**.
  
Essa propriedade é somente leitura para contas POP3 e IMAP. A tentativa de definir essa propriedade para esses tipos de contas retorna **E_ACCT_NOT_FOUND**. 
  

