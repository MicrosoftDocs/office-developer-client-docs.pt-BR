---
title: Salvando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425887"
---
# <a name="saving-mapi-properties"></a>Salvando propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitos objetos suportam um modelo de transação de processamento pelo qual as alterações nas propriedades não são permanentes até que sejam comprometidas posteriormente. Enquanto as alterações nas propriedades são manipuladas pelos métodos [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) a etapa de confirmação é manipulada por [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Não é até após uma chamada bem-sucedida para **SaveChanges** que a versão mais recente das propriedades de um objeto pode ser acessada. 
  
Quando **SaveChanges** retorna o valor de MAPI_E_OBJECT_CHANGED, este é um aviso de que outro cliente está simultaneamente compondo alterações no objeto. É possível, dependendo do provedor que está implementando o objeto, que vários clientes abram com êxito um objeto chamando seu método **OpenEntry** com o sinalizador MAPI_MODIFY definido, dando a eles acesso de leitura/gravação. O objeto retornado de tal chamada **openEntry** é um instantâneo dos dados de armazenamento. Cada tentativa subsequente de alterar esses dados pode substituir a tentativa anterior. 
  
Ao receber MAPI_E_OBJECT_CHANGED **do SaveChanges,** um cliente tem a opção de: 
  
- Faça uma cópia do objeto para manter as alterações.
    
- Faça outra chamada para **SaveChanges**, especificando FORCE_SAVE. 
    
Chamar **SaveChanges** com o FORCE_SAVE sobrescreve o salvar anterior e torna as alterações de um cliente permanentes. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

