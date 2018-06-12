---
title: Obtendo e configurando propriedades com GetProps e SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5751dc8b06d40b9f07a39f05868c328d64c27762
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766668"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtendo e configurando propriedades com GetProps e SetProps
 
**Aplica-se a**: Outlook 
  
Sempre que possível, tente recuperar ou modificar uma propriedade com os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps](imapiprop-setprops.md) . A menos que a propriedade que você estiver trabalhando com for muito grande, esses métodos devem ser adequados. A outra alternativa é ler ou gravar em um stream com a interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . Fluxos podem manipular as propriedades muito grandes com êxito, mas são um maior consumo de recursos porque eles exigem as bibliotecas de COM. Use a interface **IStream** somente depois que a chamada para **IMAPIProp::GetProps** ou **IMAPIProp::SetProps** falha. 
  

