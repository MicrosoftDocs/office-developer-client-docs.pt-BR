---
title: Obter e definir propriedades com GetProps e SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299395"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obter e definir propriedades com GetProps e SetProps
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Sempre que possível, tente recuperar ou modificar uma propriedade com os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md) A menos que a propriedade com a que você está trabalhando seja muito grande, esses métodos devem ser adequados. A outra alternativa é ler ou gravar em um fluxo com a interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Os fluxos podem lidar com propriedades muito grandes com êxito, mas são um esvaziamento maior dos recursos porque exigem as bibliotecas COM. Use a interface **IStream** somente depois que sua chamada para **IMAPIProp::GetProps** ou **IMAPIProp::SetProps falhar.** 
  

