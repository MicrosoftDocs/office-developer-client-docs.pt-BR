---
title: Salvar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770287"
---
# <a name="saving-mapi-properties"></a>Salvar propriedades MAPI

  
  
**Aplica-se a**: Outlook 
  
Muitos objetos oferecem suporte a um modelo de transação de processamento por meio da qual as alterações nas propriedades não são feitas permanentes até que sejam confirmadas mais tarde. Enquanto as alterações nas propriedades são manipuladas pelos métodos [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , a etapa de confirmação é manipulada pela [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Não é até depois de uma chamada bem sucedida a **SaveChanges** que a versão mais recente de propriedades de um objeto pode ser acessada. 
  
Quando **SaveChanges** retornará o valor de erro MAPI_E_OBJECT_CHANGED, este é um aviso de que outro cliente simultaneamente é confirmar as alterações ao objeto. É possível, dependendo do provedor de implementar o objeto, para que vários clientes com êxito, abra um objeto chamando o seu método de **OpenEntry** com o conjunto de sinalizador MAPI_MODIFY, concedendo a eles acesso de leitura/gravação. O objeto que é retornado como uma chamada **OpenEntry** é um instantâneo dos dados de armazenamento. Cada tentativa subsequente para alterar esses dados pode substituir a tentativa anterior. 
  
Ao receber MAPI_E_OBJECT_CHANGED de **SaveChanges**, um cliente tem a opção de: 
  
- Fazer uma cópia do objeto para armazenar as alterações.
    
- Fazer outra chamada para **SaveChanges**, especificando FORCE_SAVE. 
    
Chamar **SaveChanges** com o sinalizador FORCE_SAVE substitui o salvamento anterior e torna permanentes as alterações de um cliente. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

