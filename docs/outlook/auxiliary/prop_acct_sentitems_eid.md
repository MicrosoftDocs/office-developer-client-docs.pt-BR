---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa a identificação de entrada da pasta padrão para itens enviados para a conta.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766051"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Representa a identificação de entrada da pasta padrão para itens enviados para a conta. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0020  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x00200102  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Coment�rios

Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
A pasta padrão para itens enviados é **Itens enviados**.
  
Essa propriedade é somente leitura para contas POP3 e IMAP. Tentar definir essa propriedade para esses tipos de contas retorna **E_ACCT_NOT_FOUND**. 
  

