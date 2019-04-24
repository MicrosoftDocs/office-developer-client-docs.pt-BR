---
title: Salvar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283083"
---
# <a name="saving-mapi-properties"></a>Salvar propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitos objetos dão suporte a um modelo de transação de processamento em que as alterações feitas nas propriedades não são permanentes até que sejam confirmadas posteriormente. Enquanto as alterações nas propriedades são tratadas pelos métodos [IMAPIProp::](imapiprop-setprops.md) SetProps e [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) , a etapa de confirmação é manipulada por [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Ele não é até após uma chamada bem-sucedida para **SaveChanges** que a versão mais recente das propriedades de um objeto pode ser acessada. 
  
Quando **SaveChanges** retorna o valor de erro MAPI_E_OBJECT_CHANGED, este é um aviso de que outro cliente está simultaneamente confirmando alterações no objeto. É possível, dependendo do provedor que está implementando o objeto, para que vários clientes Abram com êxito um objeto chamando seu método **OpenEntry** com o sinalizador MAPI_MODIFY definido, concedendo a eles acesso de leitura/gravação. O objeto que é retornado de uma chamada **OpenEntry** é um instantâneo dos dados de armazenamento. Cada tentativa subsequente de alterar esses dados pode substituir a tentativa anterior. 
  
Após receber MAPI_E_OBJECT_CHANGED de **SaveChanges**, um cliente tem a opção de: 
  
- Faça uma cópia do objeto para armazenar as alterações.
    
- Faça outra chamada para **SaveChanges**, especificando FORCE_SAVE. 
    
Chamar o **SaveChanges** com o sinalizador FORCE_SAVE substitui o salvamento anterior e torna as alterações de um cliente permanentes. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

